---
title: الإعدادات المتقدمة لحل Invoice capture
description: توفر هذه المقالة معلومات حول الإعدادات المتقدمة في حل Invoice capture.
author: sunfzam
ms.date: 09/25/2022
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
ms.openlocfilehash: a1e24b700d0f30fd90f2619dd6e6687736a86774
ms.sourcegitcommit: 40c80a617b903c2b26e44b41147e0021c5cb680d
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 10/18/2022
ms.locfileid: "9691119"
---
# <a name="invoice-capture-solution-advanced-settings"></a>الإعدادات المتقدمة لحل Invoice capture

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

توفر هذه المقالة معلومات حول الإعدادات المتقدمة في حل Invoice capture.

## <a name="create-additional-connections-for-channels"></a>إنشاء اتصالات اضافيه للقنوات

يجب إنشاء اتصالات بالبريد الكتروني أو تخزين الملفات لتمكين مراقبه الفواتير الواردة من قنوات مختلفه. يجب تسجيل الاتصالات في بداية منح حق الوصول للتدفقات التلقائية المستخدمة في الحل.

تستخدم أنواع الاتصالات التالية لاستيراد الفواتير:

- Office 365Outlook
- Outlook.com
- OneDrive
- SharePoint

ستستخدم قناه استيراد الفاتورة الاتصالات في خطوات التكوين الاضافيه. قبل ان يتمكن المستخدمون من إنشاء قناه اتصال محدده ، يجب منح دور أمان **المسؤول** اليهم ، كما يجب ان يقوموا بإنشاء اتصالات.

لإنشاء اتصال بـ Microsoft Dataverse، اتبع هذه الخطوات.

1. انتقل إلى **نظام الإدارة \> الحل الافتراضي**.
2. حدد **‏‫جديد**، ثم حدد **مرجع الاتصال**.
3. في الحقل **عرض الاسم** ، أدخل اسمًا.
4. حدد **Microsoft Dataverse** كموصل.
5. إذا كنت تقوم باعداد الاتصال لأول مره ، فحدد **اتصالا** جديدا.
6. في مربع الحوار الذي يظهر ، قم بإنشاء ملف Dataverse اتصال ، ثم حدد **انشاء**.
7. ادخل الحساب Dataverse وكلمه المرور.
8. بعد تمرير التحقق من الصحة ، انتقل إلى صفحه الاتصال ، ثم حدد **تحديث** ، ثم حدد الحساب ، ثم حدد **إنشاء** .

لإنشاء اتصال بريد إلكتروني أو تخزين ملفات ، اتبع هذه الخطوات.

1. في الصفحة **إنشاء** الاتصال ، في الحقل **نوع** الاتصال ، حدد **Office 365Outlook**.
2. بالنسبة لاتصال البريد الإلكتروني ، يمكنك تحديد **Outlook.com** أو **Office 365 Outlook** كرابط. بالنسبة لاتصال تخزين الملفات ، يمكنك تحديد اما **OneDrive** أو **SharePoint**.

لمراجعه الاتصالات الموجودة ، انتقل إلى كائنات **الحل \> الافتراضية مراجع \> الاتصال**. يجب ان يكون لدي المستخدم الذي يقوم بإنشاء القناات اتصالا واحدا Dataverse علي الأقل بالاضافه إلى بريد الكتروني معين أو اتصالات تخزين ملفات. يجب ان يكون منشئ القناة الجديدة هو مالك الاتصال.
