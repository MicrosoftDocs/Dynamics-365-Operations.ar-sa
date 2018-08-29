---
title: "تهيئة بيانات القيم الأولية في بيئات البيع بالتجزئة الجديدة"
description: "توضح هذه المقالة البيانات التي تم إنشاؤها كجزء من عملية تهيئة Microsoft Dynamics 365 for Retail."
author: josaw1
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
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
ms.translationtype: HT
ms.sourcegitcommit: 5098fb3339403b6f2779dfe3bb7ef5c4ca78051f
ms.openlocfilehash: 80fa443fc235496a111a8a866d2e703202721268
ms.contentlocale: ar-sa
ms.lasthandoff: 08/08/2018

---

# <a name="initialize-seed-data-in-new-retail-environments"></a>تهيئة بيانات القيم الأولية في بيئات البيع بالتجزئة الجديدة

[!include [banner](includes/banner.md)]

توضح هذه المقالة البيانات التي تم إنشاؤها كجزء من عملية تهيئة Microsoft Dynamics 365 for Retail.

بعد أنه تم نشر حل البيع بالتجزئة من خلال Microsoft Dynamics Lifecycle Services ‏(LCS)، يجب عليك تهيئة تكوين البيع بالتجزئة لإنشاء بيانات التكوين الأساسية. **هام:** قبل تهيئة تكوين البيع بالتجزئة، تأكد من أنك حددت لغة وعنوان بريدي لكل كيان قانوني حيث ستقوم بإعداد متاجر البيع بالتجزئة. ويجب إكمال هذه الخطوة لكل كيان قانوني تستخدمه للبيع بالتجزئة. وتهيئة تكوين البيع بالتجزئة، اتبع الخطوات التالية.

1.  بدء عميل Dynamics 365 for Retail.
2.  انقر فوق **البيع بالتجزئة** &gt; **إعداد المقر الرئيسي** &gt; **المعلمات** &gt; **معلمات البيع بالتجزئة**.
3.  انقر فوق **تهيئة**.

تقوم التهيئة بإنشاء بيانات التكوين الافتراضية التالية:

-   الوظائف والوظائف الفرعية لمجدول البيع بالتجزئة
-   مخطط قنوات البيع بالتجزئة
-   جداول توزيع البيع بالتجزئة
-   تخطيطات الشاشة الافتراضية التي تتضمن شبكات الأزرار والصور والسمات
-   معلومات المنطقة الزمنية
-   عمليات نقطة البيع (POS)
-   أذونات نقطة البيع
-   تقارير القناة
-   بيانات تعريف السمة
-   قوالب التحقق من صحة الكيان
-   الوظيفة الدُفعية لإزالة محفوظات جلسات Commerce Data Exchange

بالإضافة إلى ذلك، يتم تمكين التسجيل المتعلق بصناعة بطاقات الدفع (PCI) لقاعدة بيانات Dynamics 365 for Retail. **ملاحظة:** هناك خيار لتكوين مجدول البيع بالتجزئة بشكل منفصل. يتيح لك هذا الخيار إعادة تعيين تكوين مجدول البيع بالتجزئة إلى الإعدادات الافتراضية الخاصة به. وبعد إتمام عملية التهيئة، يجب عليك تكوين البيانات الإضافية للبيع بالتجزئة. فيما يلي بعض الأمثلة:

-   معلمات البيع بالتجزئة
-   معلمات مجدول البيع بالتجزئة
-   قنوات البيع بالتجزئة
-   السجلات والأجهزة
-   عمليات الفرز





