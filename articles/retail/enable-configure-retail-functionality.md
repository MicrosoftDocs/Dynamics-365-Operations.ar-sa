---
title: "تهيئة بيانات القيم الأولية في بيئة بيع بالتجزئة جديدة"
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
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: 7388324fe8a9abc8fc3d723b7c8df2c73d76a2ae
ms.contentlocale: ar-sa
ms.lasthandoff: 11/03/2017

---

# <a name="initialize-seed-data-in-a-new-retail-environment"></a>تهيئة بيانات القيم الأولية في بيئة بيع بالتجزئة جديدة

[!INCLUDE [banner](includes/banner.md)]

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





