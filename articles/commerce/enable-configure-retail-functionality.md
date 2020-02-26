---
title: تهيئة بيانات القيم الأولية في بيئات البيع بالتجزئة الجديدة
description: تصف هذه المقالة البيانات التي يتم إنشاؤها كجزء من عملية تهيئة Dynamics 365 Commerce.
author: josaw1
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
ms.search.form: RetailParameters
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 49621
ms.assetid: 4dc762eb-190e-4485-8f55-b0cafc81bc37
ms.search.region: global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.openlocfilehash: e2833c32d557ec3d2dc80808222d1d47860ce6ea
ms.sourcegitcommit: 81a647904dd305c4be2e4b683689f128548a872d
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 02/01/2020
ms.locfileid: "3021521"
---
# <a name="initialize-seed-data-in-new-retail-environments"></a>تهيئة بيانات إضافة قاعدة بيانات في بيئات Retail الجديدة

[!include [banner](includes/banner.md)]

تصف هذه المقالة البيانات التي يتم إنشاؤها كجزء من عملية تهيئة Dynamics 365 Commerce.

بعد نشر حل التجارة من خلال Microsoft Dynamics Lifecycle Services (LCS)، يجب تهيئة تكوين التجارة لإنشاء بيانات التكوين الأساسية.

> [!IMPORTANT]
> قبل تهيئة تكوين التجارة، تأكد من تحديد لغة وعنوان بريدي لكل كيان قانوني حيث ستقوم بإعداد المتاجر. يجب إكمال هذه الخطوة لكل كيان قانوني تستخدمه للتجارة.

لتهيئة التكوين، اتبع الخطوات التالية.

1. ابدأ تشغيل عميل التجارة.
2. انتقل إلى **البيع بالتجزئة والتجارة** &gt; **إعداد المراكز الرئيسية** &gt; **المعلمات** &gt; **معلمات التجارة**.
3. انقر فوق **تهيئة**.

تقوم التهيئة بإنشاء بيانات التكوين الافتراضية التالية:

- الوظائف والوظائف الفرعية لمجدول التجارة
- مخطط قناة التجارة
- جداول توزيعات التجارة
- تخطيطات الشاشة الافتراضية التي تتضمن شبكات الأزرار والصور والسمات
- معلومات المنطقة الزمنية
- عمليات نقطة البيع (POS)
- أذونات نقطة البيع
- تقارير القناة
- بيانات تعريف السمة
- قوالب التحقق من صحة الكيان
- وظيفة دًفعية لحذف محفوظات جلسات عمل Commerce Data Exchange

وبالإضافة إلى ذلك، يتم تمكين التسجيل المتعلق بصناعة بطاقات الدفع (PCI) لقاعدة بيانات التجارة.

> [!NOTE]
> يوجد خيار لتكوين مجدول التجارة بصورة منفصلة. يتيح لك هذا الخيار إعادة تعيين تكوين مجدول التجارة إلى الإعدادات الافتراضية الخاصة به.

وبعد إتمام عملية التهيئة، يجب تكوين البيانات الإضافية للتجارة. فيما يلي بعض الأمثلة:

- معلمات التجارة
- معلمات مجدول التجارة
- قنوات التجارة
- السجلات والأجهزة
- عمليات الفرز
