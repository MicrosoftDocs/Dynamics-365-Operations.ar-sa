---
title: ملفات استلام Invoice capture
description: يوضح هذا المقال كيفيه تجميع ملفات الفواتير من مصادر مختلفه في Invoice capture.
author: sunfzam
ms.date: 10/13/2022
ms.topic: overview
ms.prod: ''
ms.technology: ''
ms.search.form: VendorInvoiceWorkspace, VendInvoiceInfoListPage
audience: Application User
ms.reviewer: twheeloc
ms.custom:
- "13971"
- intro-internal
ms.assetid: 0ec4dbc0-2eeb-423b-8592-4b5d37e559d3
ms.search.region: Global
ms.author: zezhangzhao
ms.search.validFrom: 2022-09-28
ms.dyn365.ops.version: ''
ms.openlocfilehash: 3c55540d11a67d4d4c4c8477d51cb6f1f5777767
ms.sourcegitcommit: 3e04f7e4bc0c29c936dc177d5fa11761a58e9a02
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 10/18/2022
ms.locfileid: "9690107"
---
# <a name="invoice-capture-received-files"></a>ملفات استلام Invoice capture

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

في Invoice capture ، تعتبر صفحه الملفات **التي** تم تلقيها مكانا مركزيا يتم فيه استلام ملفات الفواتير من مصادر مختلفه.

## <a name="upload-invoice-files"></a>تحميل ملفات الفواتير

يمكن لمشتريات الحسابات الدائنة (AP) تحميل صور الفواتير من خلال تحديد **تحميل ملف** لفتح **مربع الحوار تحميل**. بعد ان يقوم موظف AP بتحديد ملف ، يصبح الزر **تحميل** متاحا.

## <a name="include-or-obsolete-invoice-files"></a>تضمين ملفات الفواتير أو مهمله فيها

يمكن للمستخدمين تحديد الفواتير التي تحتوي علي أخطاء أو تحذيرات ، ثم اما تضمين الفواتير أو مهمله بتحديد الزر المناسب في جزء الإجراءات. لن تظهر الفاتورة التي تم وضع علامة عليها كقديمه في طريقه العرض الملفات التي **تم استلامها (أوبسوليتيد)**.

## <a name="view-captured-invoices"></a>عرض الفواتير المقيدة

بعد التعرف علي الملف الذي تم استلامه بنجاح ، يتم إرجاع معلومات الفاتورة التي تم التقاطها بواسطة نموذج الذكاء الاصطناعي ويتم إدخالها في Microsoft Dataverse. ويمكن لموظف AP بعد ذلك التحقق من تفاصيل الفاتورة من خلال تحديد **عرض الفاتورة** التي تم التقاطها. يمكن للمستخدمين تنزيل ملف الفاتورة الأصلي كما هو مطلوب.
