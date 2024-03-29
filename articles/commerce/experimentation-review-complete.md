---
title: ترقية التباين وإكمال تجربة
description: يوضح هذا المقال كيفيه ترقيه التباين الناجح وإكمال تجربه في Dynamics 365 Commerce.
author: sushma-rao
ms.date: 06/07/2022
ms.topic: article
audience: Application User
ms.reviewer: josaw
ms.search.region: Global
ms.author: sushmar
ms.search.validFrom: 2020-09-30
ms.openlocfilehash: 3e9a978551622bbb14d9213f607d9dfabe42672a
ms.sourcegitcommit: ddcb62bb5fbf26a1178c2bb1aec45a3d2362339e
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 06/07/2022
ms.locfileid: "8942727"
---
# <a name="promote-a-variation-and-complete-an-experiment"></a>ترقية التباين وإكمال تجربة

يوضح هذا المقال كيفيه ترقيه الاختلافات التي أنتجت أفضل النتائج في التجربة، وكيفيه إكمال التجربة. يوضح الرسم التخطيطي التالي كافة الخطوات المتضمنة في اعداد وتشغيل تجربه علي أحد مواقع التجارة الالكترونيه في Dynamics 365 Commerce. وتتم تغطيه الخطوات الاضافيه في مقالات منفصلة.

[ ![رحلة مستخدم التجربة - المراجعة والإكمال.](./media/experimentation_review_complete.svg) ](./media/experimentation_review_complete.svg#lightbox)

بعد [تشغيل الاختبار الخاص بك](experimentation-run-monitor.md)وتجميع البيانات الكافية لتحديد اي التغيرات التي تريد استخدامها علي موقعك المباشر، ستقوم بترقيه التباين وإنهاء التجربة.

## <a name="promote-a-variation"></a>ترقيه تباين
استخدم البيانات والتحليلات المرتبطة بالتجربة في الخدمة التابعة لجهة أخرى لتحديد الاختلافات التي أنتجت أفضل النتائج. ثم يمكنك ترقيتها عن طريق استبدال المحتوى الحالي على الموقع المباشر بالتباين الفائز بحيث يكون متوفرًا لكافة مستخدمي موقع الويب الخاص بك.

لترقية التباين الفائز، اتبع الخطوات التالية. 

1. في منشئ موقع Commerce، حدد **التجارب** في جزء التنقل الأيسر، ثم حدد التجربة.
1. على شريط الأدوات، حدد **التجربة الكاملة**.
1. في مربع حوار **إكمال التجربة**، حدد **مراجعة بيانات التجربة**. ويتم فتح الخدمة الخاصة بجهات خارجية حيث يمكنك التحقق من صحة القياسات وتحديد اي تباينات قدمت أفضل أداء.
1. في مربع حوار **إكمال التجربة**، حدد التباين الفائز، ثم حدد **التالي**.
1. افتح الخدمة التابعة لجهة أخرى وأوقف التجربة.
1. في منشئ الموقع، حدد **إكمال** للكتابة فوق الصفحة المباشرة الاصليه ونشر التباين الفائز بحيث تكون متوفرة لكافة مستخدمي موقع الويب الخاص بك. 

> [!NOTE]
> إذا اخترت الاحتفاظ بالصفحة المباشرة الحالية وعدم نشر التباين، حدد **أعاده نشر الصفحة الاصليه**.

## <a name="delete-your-experiment"></a>حذف التجربة الخاصة بك
بينما لا يتطلب ذلك حذف تجربه مكتملة في التجارة، يمكنك اختيار حذفها لتوفير مساحة أو لتنظيف مساحة العمل الخاصة بك. 

لحذف تجربة مكتملة في Commerce site builder ، اتبع هذه الخطوات.

1. حدد **تجارب** في جزء التنقل الأيسر، ثم حدد التجربة. 
    > [!NOTE]
    > في حاله استمرار نشاط التجربة، قم بإيقاف التجربة في خدمه الجهة الأخرى قبل المتابعة.
1. في شريط الأوامر، حدد **إلغاء النشر** لإزالة محتوى التباين من الموقع المباشر.
1. حدد **حذف** لحذف التجربة.

## <a name="previous-step"></a>الخطوة السابقة
[تشغيل تجربة ومراقبتها](experimentation-run-monitor.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
