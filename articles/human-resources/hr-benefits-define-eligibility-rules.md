---
title: تحديد قواعد وسياسات استحقاق الفائدة
description: تشرح هذه الموضوعات كيفية إنشاء قواعد وسياسات الأهلية للمزايا ثم تعيين قواعد للمزايا.
author: twheeloc
ms.date: 08/23/2021
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: SysPolicySourceDocumentRuleType, SysPolicyListPage, SysPolicy, HcmBenefitEligibilityPolicy, HcmBenefit, BenefitWorkspace, HcmBenefitSummaryPart
audience: Application User
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Version 7.0.0, Human Resources
ms.openlocfilehash: 4781a00ae63bb2d27df0610a1886cc43e52798f9
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 06/03/2022
ms.locfileid: "8861178"
---
# <a name="define-benefit-eligibility-rules-and-policies"></a>تحديد قواعد وسياسات استحقاق الفائدة


[!INCLUDE [PEAP](../includes/peap-1.md)]

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

توضح هذه المقالة كيفية إنشاء قواعد وسياسات الأهلية للمزايا ثم تعيين قواعد للمزايا.  

## <a name="create-benefit-eligibility-policy-rule-type"></a>إنشاء نوع قاعدة سياسة استحقاق المزايا‬

1. انتقل إلى **الموارد البشرية > الميزات > الأهلية > أنواع قواعد سياسات استحقاق الميزات**.
2. حدد **جديد**.
3. في حقل **‏‫اسم القاعدة**، أدخل قيمة.
4. في حقل **الوصف**، أدخل قيمة.
5. في الحقل  **اسم الاستعلام**، انقر فوق زر القائمة المنسدلة لفتح البحث.
6. في القائمة، حدد الارتباط في الصف المحدد.
7. حدد **حفظ**.
8. قم بإغلاق الصفحة.

## <a name="benefit-eligibility-policy"></a>سياسة استحقاق المزايا

1. انتقل إلى **الموارد البشرية > الميزات > الأهلية > سياسات استحقاق الميزات‬**.
2. حدد سياسة ميزات موجودة.
3. في القائمة، حدد الارتباط في الصف المحدد.
4. قم بتبديل توسيع الأقسام **مؤسسات السياسات‬‬**. يمكنك إضافة أي من المؤسسات التي تريد تضمينها في السياسة أو إزالتها.
5. قم بتوسيع المقطع **قواعد السياسة‬** أو طيّه.
6. في القائمة، ابحث عن "قاعدة السياسة" التي تم إنشاؤها في السابق.
7. حدد **إنشاء قاعدة السياسة**.
8. في الحقل **تاريخ السريان**، أدخل التاريخ الذي تريد أن تصبح فيه السياسة سارية المفعول.
    * يسمح لك إعداد تواريخ السريان والانتهاء بإجراء تغييرات مستقبلية على قواعد السياسة ومن ثم لا تحتاج إلى الرجوع إلى السياسة عندما تريد أن تصبح هذه التغييرات نافذة المفعول.  
9. إذا لزم الأمر ، قم بإضافة جملة where إلى حقل **إضافة شرط**.
    * على سبيل المثال، إذا أردت تطبيق القاعدة فقط على "مديري المبيعات"، فيمكنك إنشاء عبارة where للقول: حيث يساوي وصف المنصب "مدير المبيعات". يمكنك أن تضيف عبارات where متعددة في القاعدة.  
10. حدد **موافق**.
11. قم بإغلاق الصفحة.

## <a name="assign-rule-to-benefit"></a>تعيين قاعدة لميزة

1. انتقل إلى **الموارد البشرية > الميزات‬ > الميزات‬**.
2. في القائمة، قم بالبحث عن السجل المطلوب وحدده.
3. في القائمة، حدد الارتباط في الصف المحدد.
4. قم بتوسيع القسم **قواعد الاستحقاق** أو طيّه.
5. حدد **تحرير**.
6. في حقل **الأهلية**، حدد القاعدة.
7. في الحقل **نوع القاعدة**، حدد القاعدة التي أنشأتها في السابق.
9. في القائمة، حدد الارتباط في الصف المحدد.
10. حدد **حفظ**.
11. وقم بغلق النموذج.



[!INCLUDE[footer-include](../includes/footer-banner.md)]
