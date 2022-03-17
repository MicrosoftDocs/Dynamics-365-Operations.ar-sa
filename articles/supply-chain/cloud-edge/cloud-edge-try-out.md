---
title: تجريب وحدات القياس في الطوبولوجيا المختلطة الموزعة
description: يوفر هذا الموضوع معلومات حول كيفية تجربة وحدات النطاق السحابي والحافة لأحمال عمل التصنيع وإدارة المستودعات.
author: perlynne
ms.date: 03/03/2022
ms.topic: article
ms.search.form: ScaleUnitWorkloadsWorkspace
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2022-03-03
ms.dyn365.ops.version: 10.0.25
ms.openlocfilehash: 04fd79f3c582ae9ac51882f73410477efaa35496
ms.sourcegitcommit: b52ff5dfd32580121f74a5f262e5c2495e39d578
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 03/03/2022
ms.locfileid: "8376236"
---
# <a name="try-out-scale-units-in-a-distributed-hybrid-topology"></a>تجريب وحدات القياس في الطوبولوجيا المختلطة الموزعة

[!include [banner](../includes/banner.md)]

عملية تجربة الهيكل الهجين الموزع بسيطة. أثناء المرحلة الأولى، يجب عليك التحقق من صحة التخصيصات للتأكد من أنها تعمل في الهيكل الموزع. لديك خياران.

## <a name="option-1-evaluate-customizations-in-development-environments"></a>الخيار 1: تقييم التخصيصات في بيئات التطوير

قبل بدء عملية الإلحاق في بيئة الاختبار المعزولة، ننصحك باستكشاف وحدات القياس في إعداد التطوير، مثل البيئة ذات الخانة الواحدة (المعروفة أيضًا بالبيئة من المستوى 1)، بحيث يمكنك التحقق من صحة العمليات والتخصيصات والحلول. خلال هذه المرحلة، سيتم تطبيق البيانات والتخصيصات على البيئات ذات الخانة الواحدة. يمكنك التشغيل علي بيئة واحده، والتي يمكن ان تستخدم دور كل من مركز المؤسسة ووحده القياس. بدلا من ذلك، يمكن ان يكون لديك اثنين من بيئات التطوير التي تاخذ دور لوحه الوصل و الأخرى التي تاخذ دور وحده القياس. يوفر هذا الإعداد أفضل طريقة لتحديد المشكلات وإصلاحها. يمكن أيضًا [استخدام البنية الأخيرة للوصول المبكر (PEAP)](https://forms.office.com/FormsPro/Pages/ResponsePage.aspx?id=v4j5cvGGr0GRqy180BHbR56j8lZs0FdAvwT75_WNFyxURUFWTjQzTzg0UUk5RkJHMDFEMVlSSDFEQy4u) لإكمال هذه المرحلة.

يجب عليك استخدام [أدوات نشر وحدات القياس لبيئات التطوير ذات خانة واحدة](https://github.com/microsoft/SCMScaleUnitDevTools) لتثبيت البيئات وصيانتها. تتيح لك هذه الأدوات تكوين المركز ووحدات القياسي في بيئة واحدة أو بيئتين ذات خانة واحدة. يتم توفير الأدوات كإصدار ثنائي وفي كود المصدر على GitHub. ادرس wiki المشروع، الذي يشتمل على [دليل استخدام خطوة بخطوة](https://github.com/microsoft/SCMScaleUnitDevTools/wiki/Step-by-step-usage-guide) يصف كيفية استخدام الخطوات. إذا كنت [تنشر وحدات مقياس الحافة على الأجهزة المخصصة باستخدام بيانات الأعمال المحلية (LBD)](cloud-edge-edge-scale-units-lbd.md)، يجب عليك اتباع عملية مختلفة.

## <a name="option-2-acquire-add-ins-and-deploy-in-your-sandbox-environments"></a>الخيار 2: الحصول على الوظائف الإضافية ونشرها في بيئات آلية تحديد الصلاحيات الخاصة بك

لتجربة الهيكل الهجين الموزع، يجب أن يكون لديك بيئتا وضع الحماية (المستوى 2)، تحتوي إحداهما على بياناتك (مركز المؤسسة) والأخرى خاصة بوحدة المقياس وتحتوي على "بيانات فارغة".

يجب أن تحصل على الوظائف الإضافية لوحدة مقياس سحابة أو حافة واحدة على الأقل. سيتم بعد ذلك منح خانات المشاريع والبيئات المقابلة في [Microsoft Dynamics Lifecycle Services (LCS)](https://lcs.dynamics.com/)، بحيث يمكن نشر بيئات وحدة القياس باستخدام [مدخل مدير وحدة القياس](https://aka.ms/SCMSUM).

اتصل بدعم Microsoft للمطالبة بتمكين بيئات تحديد الصلاحيات.

[!INCLUDE [cloud-edge-privacy-notice](../../includes/cloud-edge-privacy-notice.md)]

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
