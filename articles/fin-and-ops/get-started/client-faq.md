---
title: الأسئلة الشائعة حول عميل Finance and Operations
description: توفر هذه المقالة إجابات على الأسئلة المتداولة حول عميل Microsoft Dynamics 365 for Finance and Operations.
author: jasongre
manager: AnnBe
ms.date: 10/23/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.custom: 12334
ms.assetid: a9a57f0e-a67c-46b1-83c9-5d6350fb3b86
ms.search.region: Global
ms.author: jasongre
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 74f85f7a1c390d1f21d0423a794ff16c7250d9fa
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 01/29/2019
ms.locfileid: "316707"
---
# <a name="finance-and-operations-client-faq"></a>الأسئلة الشائعة حول عميل Finance and Operations

[!include [banner](../includes/banner.md)]

توفر هذه المقالة إجابات على الأسئلة المتداولة حول عميل Microsoft Dynamics 365 for Finance and Operations.

## <a name="why-arent-symbols-loaded-when-i-use-finance-and-operations"></a>لماذا لا يتم تحميل الرموز عند استخدام Finance and Operations؟

قد تمنع إعدادات الأمان في المستعرض تحميل الرموز بشكل صحيح. ولحل هذه المشكلة، جرّب الخطوات التالية:

- ‏‫إذا كنت تواجه هذه المشكلة في Internet Explorer، فانقر فوق **أدوات**، ثم فوق **خيارات الإنترنت**. في مربع الحوار "خيارات الإنترنت" على علامة التبويب **الخصوصية**، انقر فوق **مستوى مخصص**، وتأكد من تحديد الخيار **تنزيل الخطوط**.
- وإلا، قد تحتاج إلى إضافة موقع Finance and Operations إلى قائمة المواقع الموثوق بها.

## <a name="i-miss-the-ribbon-from-dynamics-ax-2012-can-i-keep-action-pane-tabs-open-all-the-time"></a>‏‫أفتقد الشريط من Dynamics AX 2012. هل يمكنني الحفاظ على فتح علامات تبويب "جزء الإجراءات" على الدوام؟‬

نحن نخطط لتنفيذ هذه الميزة قريبًا. سيتمكن المستخدمون بعد ذلك من اختيار الحفاظ على علامات التبويب مفتوحة على الدوام في أجزاء الإجراءات. وإلا، سيتم طي علامات التبويب عند عدم استخدامها، للحصول على مزيد من مساحة الشاشة للصفحة.

## <a name="why-do-i-sometimes-see-different-shortcut-menus-when-i-right-click"></a>لماذا أحيانًا أرى قوائم مختصرة مختلفة عندما أنقر بزر الماوس الأيمن؟

إذا نقرت بزر الماوس الأيمن في حقل قابل للتحرير (أو في حالة تحديد نص)، فستظهر قائمة مختصرة في المستعرض. وتتيح لك هذه القائمة الوصول إلى أوامر **القص**، و**النسخ**، و **اللصق**. لا يمكننا تضمين هذه الأوامر في قوائم Finance and Operations المختصرة لأن المستعرضات لا تسمح لنا بالوصول برمجيًا إلى حافظة النظام، لأسباب أمنية.

في حالة قيامك بالنقر بزر الماوس الأيمن فوق تسمية حقل أو قيمة عنصر تحكم للقراءة فقط، فسوف تشاهد القائمة المختصرة لـ Finance and Operations.

لتسهيل الوصول إلى لوحة المفاتيح، نخطط لتطبيق اختصار لوحة مفاتيح في المستقبل سيقوم بفتح القائمة المختصرة لـ Finance and Operations.

## <a name="where-is-the-view-details-functionality-in-finance-and-operations"></a>أين توجد وظيفة عرض التفاصيل في Finance and Operations؟

يتوفر خيار **عرض التفاصيل** بطريقتين:

- إذا كان عنصر تحكم يشتمل على قدرات **عرض التفاصيل**، وإذا كان عنصر التحكم يحتوي على قيمة، فإنه يتم عرض هذه القيمة كارتباط تشعبي. يمكنك النقر فوق الارتباط التشعبي لفتح صفحة تحتوي على تفاصيل إضافية.
- **عرض التفاصيل** أيضًا عبارة عن خيار في القوائم المختصرة لـ Finance and Operations. لمزيد من المعلومات حول وقت عرض القوائم المختصرة لـ Finance and Operations عند قيامك بالنقر بزر الماوس الأيمن، راجع القسم السابق.
