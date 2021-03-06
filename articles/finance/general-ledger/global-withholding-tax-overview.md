---
title: ضريبة الخصم العمومية
description: يوفر هذا الموضوع معلومات حول وظيفة ضريبة الخصم العامة وكيفية إعدادها. يتم تحسين وظيفة ضريبة الخصم العامة لحركات المورد والعميل، بحيث يتم حساب ضريبة الخصم على مستوى الصنف.
author: roschlom
manager: AnnBe
ms.date: 01/12/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.custom: 15721
ms.assetid: b4b406fa-b772-44ec-8dd8-8eb818a921ef
ms.search.region: Global
ms.author: kailiang
ms.search.validFrom: 2020-01-12
ms.dyn365.ops.version: AX 10.0.16
ms.openlocfilehash: 17ed1dcae97f6cd28175c483be5ca3ce96d59e05
ms.sourcegitcommit: 053f4cda6862fbcd9e3aa6e9cb009e7de833beac
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 01/28/2021
ms.locfileid: "5075728"
---
# <a name="global-withholding-tax"></a>ضريبة الخصم العمومية

[!include [banner](../includes/banner.md)]

يوفر هذا الموضوع معلومات حول وظيفة ضريبة الخصم العامة ويشرح كيفية إعدادها. تتوفر الوظيفة الجديدة في الإصدار 10.0.17 والإصدارات اللاحقة.

يتم تحسين وظيفة ضريبة الخصم العامة لحركات المورد والعميل، بحيث يتم حساب ضريبة الخصم على مستوى الصنف. يمكن تسوية الرصيد في حساب ضريبة الخصم من حركات الشراء من خلال تشغيل مهمة دفع ضريبة الخصم مقابل حساب تسوية ضريبة الخصم.

> [!NOTE]
> لا تدعم ضريبة الخصم العامة وظيفة **الاحتفاظ بالتكاليف** في صفحات أمر الشراء وفاتورة المورد وأمر المبيعات.

## <a name="turn-on-global-withholding-tax"></a>تشغيل ضريبة الخصم العمومية

1. في مساحة عمل **إدارة الميزات**، حدد **ضريبة الخصم العمومية**، ثم حدد **تمكين الآن**.
2. انتقل إلى **الضريبة \> الإعداد \> المعلمات \> معلمات دفتر الأستاذ العام**، ثم ، في علامة التبويب **ضريبة الخصم**، قم بتعيين خيار **تمكين ضريبة الخصم العامة** إلى **نعم**.
3. حدد **حفظ**.
4. قم بتحديث الصفحة في مستعرض الويب الخاص بك.

> [!NOTE]
> لا يمكن تشغيل وظيفة ضريبة الخصم العالمية للبلدان/المناطق التي توجد فيها حلول ضريبة الخصم المترجمة بالفعل. وتتضمن هذه المناطق ولكن لا تقتصر على الهند والبرازيل وتايلاند والمملكة العربية السعودية والبرازيل والبريطانيا العظيمة والولايات المتحدة.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]