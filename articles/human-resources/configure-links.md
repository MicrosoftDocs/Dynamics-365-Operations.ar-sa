---
title: إنشاء ارتباطات من Human Resources إلى بيئة أخرى
description: توضح هذه المقالة كيفية إنشاء ارتباط من Microsoft Dynamics 365 Human Resources إلى بيئة Dynamics 365 أخرى.
author: twheeloc
ms.date: 03/18/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2021-29-11
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 9640f460ed7b0b1a0cfdffb7c318bf833f8627fc
ms.sourcegitcommit: 28a726b3b0726ecac7620b5736f5457bc75a5f84
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 06/29/2022
ms.locfileid: "9065282"
---
# <a name="create-links-from-human-resources-to-another-finance-environment"></a>إنشاء ارتباطات من Human Resources إلى بيئة Finance أخرى

من المحتمل وجود بيئتين في Dynamics 365 لدى العميل يعمل عليهما: على سبيل المثال، قد يكون لدي العميل بيئة Dynamics 365 Human Resources في بنية Finance الأساسية ويحتاج إلى الاتصال ببيئة Dynamics 365 Finance أخرى. 

ستسمح هذه الميزة بارتباطات من صفحه Human Resources إلى صفحه معينة في بيئة Finance أخرى. عند تكوين الارتباطات، يمكنك تحديد المكان الذي سيتوفر فيه الارتباط في Human Resources، والصفحة الهدف التي سيتم فتحها في البيئة الأخرى.

> [!Note] 
> يجب تشغيل **تحسينات تجربة مستخدم الموارد البشرية‬** في **إدارة الميزات** للحصول على هذه الميزة.

## <a name="configure-target-systems"></a>تكوين الأنظمة الهدف

في Human Resources، بإمكان مسؤولي النظام تعريف الارتباطات التي ستظهر في صفحات **Human Resources**. تشكّل بيئات Finance التي تريد الانتقال إليها على أنها "هدف" الارتباط جزءًا من التكوين. 

لتكوين النظام الهدف:
1. في الصفحة **تكوين الارتباطات**، حدد **تكوين النظام الهدف**.  
2. أدخل اسم النظام الهدف وأدخل عنوان URL لبيئة Finance. بعد تكوين الأنظمة الهدف، يمكنك تعريف الارتباطات.

## <a name="configure-links"></a>تكوين الارتباطات

سيتم تعريف المعلومات التالية لكل ارتباط تقوم بإنشائه:
 - **ارتباط**: اسم الارتباط. يُستخدم بهدف التعريف فقط.
 - **تمكين هذا الارتباط**: عيّن هذا الخيار إلى **نعم** إذا أردت عرض الارتباط لمستخدمي Human Resources.
 - **الاسم المعروض**: أدخل الاسم الذي سيظهر كارتباط إلى البيئة الثانوية. 
 - **إظهار الارتباط على النموذج**: اختر الصفحة التي تريد عرض الارتباط عليها. يمكن إظهار الارتباطات فقط في مساحة عمل **خدمة الموظف الذاتية** وصفحات **الوظيفة** و **المنصب** و **العامل** و **العامل المبسط**.
 - **المجموعة**: يمكنك تنظيم الارتباطات باستخدام المجموعات. حدد مجموعة موجودة، أو أنشئ مجموعة جديده باستخدام عمود **المجموعة**.
 - **النظام الهدف**: حدد النظام الهدف الذي تم إنشاؤه باستخدام الخيار **تكوين النظام الهدف**. سيكون هذا البيئة الثانوية لتي سيتم استخدامها عند التنقل باستخدام الارتباط.
 - **استخدام الشركة الحالية للمستخدم**: حدد **نعم‏‎** لاستخدام الشركة الحالية للمستخدم‬ عند الانتقال إلى Finance. حدد **لا** لتحديد الشركة التي يجب استخدامها.
 - عنصر قائمة **الهدف‬**: أدخل عنصر القائمة من بيئة Finance الذي يجب أن يستخدمه الارتباط عند التنقل. تتوفر عناصر القائمة التي يمكنك الانتقال إليها مباشرة. 

   للعثور علي عنصر القائمة المطلوب:
   1. انتقل إلى بيئة Finance وافتح الصفحة التي تعتبر هدف التنقل. 
   2. انسخ عنصر القائمة من عنوان URL. على سبيل المثال، إذا أردت أن ينقلك الارتباط إلى قائمة الموظفين في التمويل والعمليات، فأدخل القيمة التي تظهر بعد "&mi" في عنوان URL. 
   3. عنصر القائمة للانتقال إليه في صفحة قائمة الموظفين في هذا المثال هو: HcmWorkerListPage_Employees.

 - **ارتباط بمصدر البيانات**: - حدد مصدر البيانات الذي يشير إليه الارتباط. تتوفر المصادر الأكثر شيوعًا مثل **العامل** و **المنصب**.

### <a name="access-to-links"></a>الوصول إلى الارتباطات

سوف يرى مسؤولو النظام الارتباطات التي تم إنشاؤها حديثًا على الصفحات المحددة حتى لو تم تعيين الخيار **تمكين هذا الارتباط** إلى **لا**. يمكن استخدام هذا لاختبار الارتباطات قبل إظهارها للموظفين الآخرين. ستتمكن كافة الأدوار الأخرى من رؤية الارتباطات الأخرى فقط بعد تعيين الخيار **تمكين هذا الارتباط** إلى **نعم**. سيتمكن الموظفون الذين يمكنهم الوصول إلى الصفحات التي تظهر فيها الارتباطات من الوصول إلى الارتباطات.

يجب أن يكون لدى المستخدمين أيضًا حقوق أمان داخل البيئة الثانوية المحددة للوصول إلى الصفحات الموجودة في تلك البيئة. إذا لم تتوفر لديهم مثل هذه الحقوق، فسيظهر مربع حوار أمان عند استخدام الارتباط.


