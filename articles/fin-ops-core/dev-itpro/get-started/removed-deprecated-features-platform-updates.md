---
title: ميزات Platform التي تمت إزالتها أو إهمالها
description: يصف هذا الموضوع الميزات التي تمت إزالتها أو تلك المخطط لإزالتها في تحديثات الأنظمة الأساسية لتطبيقات Finance and Operations.
author: sericks007
manager: AnnBe
ms.date: 02/25/2019
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
ms.openlocfilehash: 66e1420c7053c0df9f42b15c55aba1a8c869f02a
ms.sourcegitcommit: 2cc3b89efdd90f8d80883b7a271d7885282ba3e8
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 02/26/2020
ms.locfileid: "3087873"
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

## <a name="previous-announcements-about-removed-or-deprecated-features"></a>الإعلانات السابقة حول الميزات التي تمت إزالتها أو إهمالها
لمعرفه المزيد حول الميزات التي تمت إزالتها أو إهمالها في الإصدارات السابقة، راجع [‏‫الميزات التي تمت إزالتها أو إهمالها في الإصدارات السابقة‬](../migration-upgrade/deprecated-features.md).

