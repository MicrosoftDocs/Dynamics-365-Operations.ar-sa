---
title: "مسح الأكواد الشريطية باستخدام الكاميرا في Dynamics 365 for Finance and Operations – Warehousing"
description: "يشرح هذا الموضوع كيفية إعداد Dynamics 365 for Finance and Operations – Warehousing لمسح الأكواد الشريطية باستخدام كاميرا على جهاز محمول."
author: MarkusFogelberg
manager: AnnBe
ms.date: 01/03/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: WHSMobileAppField
audience: Application User
ms.reviewer: bis
ms.search.scope: Core, Operations
ms.custom: 269384
ms.search.region: Global
ms.author: mafoge
ms.search.validFrom: 2017-01-03
ms.dyn365.ops.version: AX 8.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7be3e9970e2599c159e7c9d414b54876d0116350
ms.openlocfilehash: f7fe3ab07578b09822fbfeaa4b07331b79f13610
ms.contentlocale: ar-sa
ms.lasthandoff: 03/09/2018

---

# <a name="scan-bar-codes-using-a-camera-in-dynamics-365-for-finance-and-operations--warehousing"></a>مسح الأكواد الشريطية باستخدام الكاميرا في Dynamics 365 for Finance and Operations – Warehousing

[!INCLUDE [banner](../includes/banner.md)]

يشرح هذا الموضوع كيفية إعداد Dynamics 365 for Finance and Operations – Warehousing لمسح الأكواد الشريطية باستخدام كاميرا على جهاز محمول. 

## <a name="prerequisites"></a>المتطلبات الأساسية
لاستخدام هذه الميزة، يجب أن يكون الإصدار 1.2.0.0 من تطبيق Warehousing مثبتًا لديك، ويجب أن يتضمن جهازك كاميرا. عندما تفتح التطبيق بعد التحديث، سيتم مطالبتك بالسماح لتطبيق Dynamics 365 for Finance and Operations – Warehousing باستخدام الكاميرا. في حال عدم وجود كاميرا في جهازك، لن تظهر أي مطالبة، وسيتعذر عليك استخدام الكاميرا كماسح ضوئي. 

## <a name="setup"></a>إعداد
في "إعدادات العرض" الخاصة بالتطبيق Warehousing، يمكنك تحديد ما إذا كان يجب استخدام الكاميرا لمسح الأكواد الشريطية. إذا قمت بتمكين الخيار **استخدام الكاميرا كماسح ضوئي**، فيمكنك استخدام الكاميرا في كل حقل إدخال تم فيه تعيين وضع الإدخال المفضل إلى **مسح ضوئي**. 

للتحكم في ما إذا كان يجب أن يكون حقل الإدخال قابلاً للمسح الضوئي، في صفحة **أسماء حقول تطبيق المستودع‬** في Dynamics 365 for Finance and Operations، قم بتعيين **وضع الإدخال المفضل** إلى **مسح ضوئي**. عند تحديد هذا الخيار، يمكن استخدام كاميرا لإجراء مسح ضوئي في تطبيق Warehousing. لمزيد من المعلومات حول كيفية تكوين أسماء حقول التطبيق في Warehousing، راجع [تكوين أسماء حقول التطبيق في تطبيق Warehousing](https://docs.microsoft.com/en-us/dynamics365/unified-operations/supply-chain/warehousing/configure-app-field-names-priorities-warehouse).

## <a name="supported-bar-code-formats"></a>تنسيقات الأكواد الشريطية المدعومة
يتم اعتماد تنسيقات الأكواد الشريطية الأكثر شيوعًا، بما فيها الكود 128 والكود 39 والكود 93 والأكواد EAN-8 وEAN-13 وUPC-E وUPC-A وQR. 

## <a name="navigation"></a>التنقل
سيتم بدء صفحة الكاميرا على كل صفحة حيث تم تعيين وضع الإدخال المفضل لحقل الإدخال إلى "مسح ضوئي". عند وجودك في صفحة الكاميرا، استخدم الخيارات التالية للتنقل:
- انقر فوق زر السابق للعودة إلى صفحة "المهمة والتفاصيل". 
- انقر فوق القلم في صفحة "المهمة والتفاصيل" للانتقال إلى الصفحة حيث يمكنك كتابة الإدخال يدويًا.
- انقر فوق الكاميرا في الصفحة "المهمة والتفاصيل" للرجوع إلى صفحة الكاميرا. 

| صفحة المهمة والتفاصيل | صفحة الكاميرا | 
| :---------------------: | :--------------------: |
| ![camera-scanning-example-task-detail-page](./media/camera-scanning-example-task-detail-page50.png)          | ![camera-scanning-example-camera-page-smaller](./media/camera-scanning-example-camera-page50.png)          |

في صفحة الكاميرا، عندما تنقر فوق زر "الكاميرا"، سوف يظهر خافتًا أثناء محاولة تحديد كود شريطي. إذا لم يتم تحديد كود شريطي في غضون 5 ثوان، فستنتهي مهلة العملية وسيصبح زر الكاميرا متوفرًا من جديد. بعد ذلك، سيكون بإمكانك محاولة مسح كود شريطي مرة أخرى.

عندما تقوم بتوجيه الكاميرا نحو كود شريطي، اعمل على إبقاء الكود الشريطي في وضع المحاذاة داخل الأقواس للحصول على أفضل النتائج. عندما يتم مسح كود شريطي بنجاح، ستتم معالجة النتيجة، وسيتم نقلك إلى الخطوة التالية. إذا احتوت الخطوة التالية على حقل إدخال آخر تم فيه تعيين وضع الإدخال المفضل إلى "مسح ضوئي"، فستبدأ صفحة الكاميرا من جديد. إذا لم تكن الخطوة التالية عبارة عن حقل مسح، فلن تبدأ عندئذٍ صفحة الكاميرا.


