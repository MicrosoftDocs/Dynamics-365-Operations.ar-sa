---
title: "توسيع وظائف Microsoft Dynamics 365 for Talent"
description: "إذا قمت بإنشاء أي Microsoft PowerApps، فإنه يمكنك بدء تشغيل تلك التطبيقات من الارتباطات الموجودة في Microsoft Dynamics 365 for Talent."
author: rschloma
manager: AnnBe
ms.date: 03/21/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: rschloma
ms.search.scope: Talent
ms.custom: 17271
ms.assetid: ba1ad49d-8232-400e-b11f-525423506a3f
ms.search.region: Global
ms.author: rschloma
ms.search.validFrom: 2017-11-28
ms.dyn365.ops.version: Talent July 2017 update
ms.translationtype: HT
ms.sourcegitcommit: 72d4ff5e1311005d3bf43a13e28208cd9b3d1457
ms.openlocfilehash: 51eb4288f5b6c732755007c1dcd8c4db090ccc0a
ms.contentlocale: ar-sa
ms.lasthandoff: 03/07/2018

---
# <a name="extend-the-functionality-of-microsoft-dynamics-365-for-talent"></a>توسيع وظائف Microsoft Dynamics 365 for Talent

[!include [banner](includes/banner.md)]

إذا قمت بإنشاء أي Microsoft PowerApps، فإنه يمكنك بدء تشغيل تلك التطبيقات من الارتباطات الموجودة في Microsoft Dynamics 365 for Talent. لإعداد وصول إلى التطبيقات الخاصة بك، ستحتاج إلى إعداد بعض المعلومات في Talent في صفحة تكوين يمكنك فتحها من مساحة عمل **إدارة النظام**.

## <a name="configuring-embedded-powerapps-within-talent"></a>تكوين PowerApps المضمن داخل Talent
استخدم صفحة **تعيين Microsoft PowerApps المضمنة** لتكوين صفحات Talent لبدء تشغيل تطبيقات PowerApps. لفتح صفحة **تعيين Microsoft PowerApps المضمنة**، افتح مساحة عمل **إدارة النظام**، ثم افتح علامة التبويب **ارتباطات**. حدد **Microsoft PowerApps** من مجموعة **الإعداد**. 

يتم إدخال المعلومات التالية أو تعيينها في هذه الصفحة: 

 -  اسم وصفي أو معرف لكل تطبيق PowerApps.
 -  معرف فريد (GUID) لكل تطبيق تضيفه إلى صفحة Talent. معرف التطبيق متوفر على موقع PowerApps، [powerapps.com](http://powerapps.com/). 
 -  الصفحة التي يستطيع المستخدمون منها فتح تطبيق أو تقرير. لا تدعم جميع صفحات Talent تطبيقات PowerApps المضمنة وتقارير Power BI. 

 > [!NOTE]
 >  أدخل الاسم الداخلي للصفحة بدلاً من اسم العرض الذي يظهر في أعلى الصفحة. للعثور على الاسم الداخلي، افتح الصفحة التي تحتاج إلى اسمها الداخلي، وانقر نقرًا مزدوجًا فوق أي مكان على الصفحة. عند فتح القائمة، قم بالتمرير فوق عنصر **معلومات النموذج**. يتم عرض اسم النموذج الداخلي بجوار عنصر **معلومات النموذج** في القائمة.
 
-   حدد عنصر تحكم النموذج الذي يمكن للتطبيق استرداد بيانات السياق منه. على سبيل المثال، قد يستخدم تطبيق بيانات حول عامل. إذا قمت بإدخال صفحة **العامل** في حقل **السياق**، فسيتم فتح صفحة **العامل** عند بدء تشغيل التطبيق. إدخال في **حقل السياق** اختياري. 
-   قم بتعيين حجم مربع الحوار الذي سيتم تشغيل تطبيق PowerApps عليه. تم تعيين مربعات الحوار كـ "صغيرة" أو "كبيرة" لتحسين واجهة عند قيامك بتشغيل تطبيق على هاتف أو جهاز أكبر، على التوالي. 


يمكنك أيضًا تحديد الكيانات القانونية التي سيكون أحد التطبيقات متوفرًا لها، أو يمكنك توفيرها لجميع الكيانات القانونية. بشكل افتراضي، تتوفر تطبيقات PowerApps لجميع الكيانات القانونية.

## <a name="opening-an-application"></a>فتح تطبيق
عندما تنتهي من تكوين تطبيقات PowerApps المضمنة، ستتم إضافة ارتباطات خاصة بالتطبيقات التي حددتها إلى الصفحات داخل Talent. انقر فوق ارتباط لفتح تطبيق. 



