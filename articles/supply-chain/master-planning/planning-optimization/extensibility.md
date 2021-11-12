---
title: قابلية توسعة تحسين التخطيط‬
description: يصف هذا الموضوع سيناريوهات القابلية للتوسعة المدعومة في تحسين أداء التخطيط.
author: ChristianRytt
ms.date: 08/05/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ReqCreatePlanWorkspace
audience: Application User, Developer, IT Pro
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2020-07-07
ms.dyn365.ops.version: 10.0.13
ms.openlocfilehash: e18801a02ae9e904eb5bc597f9f61ed42c537ab9
ms.sourcegitcommit: 614d79cba238e466d445767a7d0a012e785a9861
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 10/19/2021
ms.locfileid: "7651917"
---
# <a name="planning-optimization-extensibility"></a>قابلية توسعة تحسين التخطيط‬

[!include [banner](../../includes/banner.md)]

يصف هذا الموضوع سيناريوهات القابلية للتوسعة ذات الصلة بالتخطيط الرئيسي والمدعومة في تحسين أداء التخطيط. إمكانيات البحث المتصلة بالسحابة هذه متوفرة للبدء في الإصدار 10.0.13 من Microsoft Dynamics 365 Supply Chain Management.

## <a name="custom-processing-when-master-planning-is-completed"></a>معالجه مخصصه عند اكتمال التخطيط الرئيسي

في سيناريو القابلية للتوسعة الأكثر شيوعا في تحسين التخطيط ، يتم اجراء معالجه مخصصه بعد تحديث الخطة. علي سبيل المثال ، ربما تقوم باضافه عمود إلى جدول الأوامر المخططة (`ReqPO`) ، أو قد ترغب في اشتقاق بعض المعلومات الاحصائيه من الخطة التي تم إنشاؤها. نقطه القابلية للتوسعة الرئيسية التي تمكن هذه السيناريوهات هو أسلوب `jobCompletedSuccessfully` في الفئة `MpsMasterPlanningEvents`.

```X++
public static void jobCompletedSuccessfully(MpsMasterPlanningJobCompletedSuccessfullyEventArgs _args)
```

وفيما يلي مثال علي الملحق الذي يقوم بتعيين حقل `CstmOrderPriority` مخصص في الأمر المخطط.

```X++
[ExtensionOf(classStr(MpsMasterPlanningEvents))]
public static final class MpsMasterPlanningEvents_Cstm_Extension
{
    public static void jobCompletedSuccessfully(MpsMasterPlanningJobCompletedSuccessfullyEventArgs _args)
    {
        ttsbegin;

        var affectedPlannedOrdersQuery = _args.parmPostProcessingQueryBuilder().buildAffectedPlannedOrdersQuery();
        var affectedPlannedOrdersQueryRun = new QueryRun(affectedPlannedOrdersQuery);

        while (affectedPlannedOrdersQueryRun.next())
        {
            ReqPO reqPO = affectedPlannedOrdersQueryRun.get(tableNum(ReqPO));
            reqPO.selectForUpdate(true);
            reqPO.CstmOrderPriority = reqPO.ReqDate - systemDateGet() < 7 ? CstmPlannedOrderPriority::Urgent : CstmPlannedOrderPriority::Regular;
            reqPO.doUpdate();
        }

        ttscommit;

        next jobCompletedSuccessfully(_args);
    }

}
```

عند أضافه منطق مخصص ، يجب مراعاه القيود وأفضل الممارسات التالية:

- يتم استدعاء الأسلوب `jobCompletedSuccessfully` خارج نطاق الحركة. لذلك ، تكون الخطة مرئية بالفعل للمستخدم عند بدء تشغيل المنطق المخصص. في حاله قيام التخصيص بتعيين حقول اضافيه في الأوامر المخططة ، فانه من المهم السماح للمستخدمين بمعرفه ان قيم هذه الحقول ستكون في النهاية متسقة (بمعني آخر ، قد تكون قديمه بعد اكتمال مهمة التخطيط مباشره).
- يمكن ان تبدا وظيفة تخطيط رئيسيه أخرى عند استدعاء الأسلوب `jobCompletedSuccessfully`. قد تؤثر الوظيفة الجديدة علي الخطة الكاملة أو جزء من الخطة. قد تقوم الوظيفة الجديدة بتحديث أو حذف نفس الأوامر المخططة أو حركات المتطلبات التي تم إنشاؤها أو تحديثها كجزء من مهمة التخطيط التي تمت معالجتها في `jobCompletedSuccessfully`. يجب معالجه استثناءات تعارض التحديث عند توسيع هذا الحدث.
- تجنب استخدام نطاق العمليات المفردة عند توسيع هذا الأسلوب. يمكن ان يؤدي تشغيل تخطيط رئيسي مفرد إلى الملايين من حركات الاحتياجات والمئات من آلاف الأوامر المخططة. في حاله معالجه كافة هذه الحركات والأوامر المخططة في نطاق عمليه واحده ، ستحدث العديد من عمليات تامين SQL وحظر عمليات التخطيط الأخرى. بالاضافه إلى ذلك ، في حاله الاحتفاظ بالحركة لفتره طويلة ، سيتم إنشاء "السجلات الخفية" في قاعده بيانات SQL. وسوف تؤثر السجلات الخفية بشكل سلبي علي كل عمليه في النظام.


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]