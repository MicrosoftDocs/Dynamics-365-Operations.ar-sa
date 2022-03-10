---
title: إنشاء أمر مبيعات لمنتج قابل للتكوين
description: يوضح هذا الإجراء كيفية تطبيق قالب تكوين على منتج في أمر مبيعات.
author: t-benebo
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: DefaultDashboard, SalesOrderProcessingWorkspace, SalesCreateOrder, SalesTable, PCRuntimeConfigurator, PCTemplateConfigurationSelection
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: benebotg
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: e42f121d1efa66f85a3dd811606962b907ed177d
ms.sourcegitcommit: 3b87f042a7e97f72b5aa73bef186c5426b937fec
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 09/29/2021
ms.locfileid: "7570575"
---
# <a name="create-a-sales-order-for-a-configurable-product"></a>إنشاء أمر مبيعات لمنتج قابل للتكوين

[!include [banner](../../includes/banner.md)]

يوضح هذا الإجراء كيفية تطبيق قالب تكوين على منتج في أمر مبيعات. يستخدم هذا المثال نموذج مكبر الصوت المتطور D0006 في شركة بيانات العرض التوضيحي USMF. يستخدم معالج أمر المبيعات عادةً هذا الإجراء.

## <a name="create-a-sales-order"></a>إنشاء أمر مبيعات

1. انتقل إلى **المبيعات والتسويق \> مساحات العمل \> معالجة أوامر المبيعات والاستعلام عنها**.
1. حدد **جديد**.
1. حدد **أمر المبيعات**.
1. في حقل **حساب العميل**، حدد *US-001*. 
1. حدد **موافق**.
1. في حقل **رقم الصنف**، حدد *D0006*.
    * لتنفيذ هذه المهمة، يجب تحديد منتج قابل للتكوين.  
1. حدد **المنتج والتوريد**.
1. حدد **تكوين البند**.
    * لاحظ أن السعر قد تغيّر، استنادًا إلى التكوين الذي تم تحديده، وأن الحقل **تضمين الكبل** أصبح الآن معينًا إلى *True*.  
    * لاحظ أنه تم تحديد السعر الافتراضي والإعدادات للكبل.  
1. حدد **تحميل قالب**.
    * يوضح هذا المثال كيفية تطبيق قالب لتحديد تكوين معرّف مسبقًا. إذا كنت تستخدم هذا الإجراء كدليل مهمة وأردت رؤية قيم السمات الأخرى المتوفرة، فيجب تحديد الزر **إلغاء قفل**.  
1. حدد **موافق**.
1. حدد **موافق**.
1. قم بتوسيع قسم **تفاصيل البند**.
1. حدد علامة التبويب **منتج**.
    * تم الآن إدراج تكوين الصنف ضمن أبعاد المنتج.  
1. قم بإغلاق الصفحة.


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]