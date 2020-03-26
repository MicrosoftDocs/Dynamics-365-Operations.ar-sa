---
title: ميزات Platform التي تمت إزالتها أو إهمالها
description: يصف هذا الموضوع الميزات التي تمت إزالتها أو تلك المخطط لإزالتها في تحديثات الأنظمة الأساسية لتطبيقات Finance and Operations.
author: sericks007
manager: AnnBe
ms.date: 03/03/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: sericks
ms.search.scope: Operations
ms.search.region: Global
ms.author: sericks
ms.search.validFrom: 2020-02-29
ms.dyn365.ops.version: Platform update 33
ms.openlocfilehash: d394f5ca84efc5beb943d349e45a3d2c9639d83c
ms.sourcegitcommit: 75974ae567bb0eacf0f65cac992b34ce5c680b93
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 03/03/2020
ms.locfileid: "3095764"
---
# <a name="removed-or-deprecated-platform-features"></a>ميزات Platform التي تمت إزالتها أو إهمالها

[!include [banner](../includes/banner.md)]

يصف هذا الموضوع الميزات التي تمت إزالتها أو تلك المخطط لإزالتها في تحديثات الأنظمة الأساسية لتطبيقات Finance and Operations.

- لم تعد ميزة *تمت الإزالة* متوفرة في المنتج.
- لا توجد ميزة *المهملة* في التطوير النشط وقد يتم إزالتها في تحديثات مستقبلية.

تهدف هذه القائمة إلى مساعدتك في مراعاة ميزات الإزالة وعمليات الإهلاك للتخطيط الخاص بك. 

> [!NOTE]
> يمكن العثور على معلومات مفصلة حول الكائنات في تطبيقات Finance and Operations [التقارير المرجعية التقنية](https://mbs.microsoft.com/customersource/northamerica/AX/downloads/reports/axtechrefrep). يمكنك مقارنة إصدارات مختلفة من هذه التقارير لمعرفة المزيد حول الكائنات التي تم تغييرها أو التي تمت إزالتها من كل إصدار من تطبيقات Finance and Operations.

## <a name="platform-update-32"></a>update 32 للنظام الأساسي

### <a name="workflow-request-change-dialog-box-no-longer-includes-user-selection-drop-down-list"></a>لم يعد مربع حوار تغيير طلب سير العمل يتضمن القائمة المنسدلة لتحديد المستخدم
|   |  |
|------------|--------------------|
| **سبب الإهلاك/الإزالة** | كانت هذه مشكلة تتعلق بالأمان نظرا لأنه قد تم إرسال طلب التغيير إلى مستخدم غير مقصود. وكانت كذلك مشكلة في الاستخدام لأنها أجبرت المستخدم على تحديد الشخص الذي أنشأ سير العمل ويقوم بتحديدها يدويا.  |
| **هل تم الاستبدال بميزة أخرى؟**   | لا |
| **مناطق المنتجات المتأثرة**         | سير العمل |
| **خيارات النشر**              | الكل |
| **الحالة**                         | تمت إزالة القائمة المنسدلة لتحديد المستخدم من مربع حوار طلب التغيير في النظام الأساسي لتحديث النظام 32. سيتم إرسال طلبات التغيير التي تم طلبها تلقائيا إلى المنشئ كما هو مطلوب. لمزيد من المعلومات حول هذ الوظيفة، راجع [‏‫الإجراءات في عمليات الموافقة على سير العمل](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/organization-administration/workflow-actions?toc=%2Fdynamics365%2Fcommerce%2Ftoc.json#request-change). |

### <a name="embedded-drill-through-links-are-no-longer-supported-in-paginated-documents-rendered-by-the-cloud-hosted-service"></a>لم تعد الارتباطات المستخدمة للتصفح مدعومة في المستندات ذات حدود فاصلة للصفحات التي تعرضها الخدمة المستضافة في السحابة 
|   |  |
|------------|--------------------|
| **سبب الإهلاك/الإزالة** | قد تحتوي عناوين URL المضمنة في المستندات التي تعرضها الخدمة على بيانات عمل حساسة. نحن نعمل على إزالة دعم الارتباطات المستخدمة للتصفح في المستندات كتدبير وقائي لتوفير المزيد من الحماية لبيانات العميل. سيستفيد المستخدمون أيضًا من الأداء المحسن أثناء إنتاج المستندات بشكل تفاعلي كنتيجة لهذا التغيير.  |
| **هل تم الاستبدال بميزة أخرى؟**   | لا |
| **مناطق المنتجات المتأثرة**         | التقارير |
| **خيارات النشر**              | ‏‏الكل |
| **الحالة**                         | تمت إزالة هذه الميزة من الخدمة.<br><br>يقدم العميل الحديث خيارات عديدة لإنتاج طرق العرض التي تتضمن ارتباطات يتم إنشاؤها تلقائيًا للمساعدة في التنقل في التطبيق. ننصح بالمستندات ذات حدود فاصلة للصفحات التي تعرضها الخدمة للمراسلات الخارجية التي يتم إرسالها بالبريد الإلكتروني وأرشفتها وطباعتها للمستلمين. لقد قمنا بتحسين تجربة معاينة المستندات مباشرة في المستعرض، مما يوفر الوصول المباشر إلى الطابعات المحلية. لمزيد من المعلومات، راجع [معاينة مستندات PDF باستخدام عارض مضمن‬](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/analytics/preview-pdf-documents). |

## <a name="previous-announcements-about-removed-or-deprecated-features"></a>الإعلانات السابقة حول الميزات التي تمت إزالتها أو إهمالها
لمعرفه المزيد حول الميزات التي تمت إزالتها أو إهمالها في الإصدارات السابقة، راجع [‏‫الميزات التي تمت إزالتها أو إهمالها في الإصدارات السابقة‬](../migration-upgrade/deprecated-features.md).

