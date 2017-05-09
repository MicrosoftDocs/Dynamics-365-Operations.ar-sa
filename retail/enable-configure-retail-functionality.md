---
title: "تهيئة بيانات القيم الأولية في بيئة بيع بالتجزئة جديدة"
description: "توضح هذه المقالة البيانات التي تم إنشاؤه كجزء من عملية التهيئة لـ Microsoft Dynamics 365 for Operations - البيع بالتجزئة."
author: josaw1
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User
ms.reviewer: annbe
ms.search.scope: AX 7.0.0, Operations, Core, Retail
ms.custom: 49621
ms.assetid: 4dc762eb-190e-4485-8f55-b0cafc81bc37
ms.search.region: global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 0c6a7bdc4ba82dd57ab3e395e6dfb0ae4de31fc4
ms.openlocfilehash: 137c675781cf75d9ce621a84c89224019c161362
ms.lasthandoff: 03/31/2017


---

# <a name="initialize-seed-data-in-a-new-retail-environment"></a>تهيئة بيانات القيم الأولية في بيئة بيع بالتجزئة جديدة

[!include[banner](includes/banner.md)]


توضح هذه المقالة البيانات التي تم إنشاؤه كجزء من عملية التهيئة لـ Microsoft Dynamics 365 for Operations - البيع بالتجزئة.

بعد أنه تم نشر حل البيع بالتجزئة من خلال Microsoft Dynamics Lifecycle Services ‏(LCS)، يجب عليك تهيئة تكوين البيع بالتجزئة لإنشاء بيانات التكوين الأساسية. **هام:** قبل تهيئة تكوين البيع بالتجزئة، تأكد من أنك حددت لغة وعنوان بريدي لكل كيان قانوني حيث ستقوم بإعداد متاجر البيع بالتجزئة. ويجب إكمال هذه الخطوة لكل كيان قانوني تستخدمه للبيع بالتجزئة. وتهيئة تكوين البيع بالتجزئة، اتبع الخطوات التالية.

1.  بدء عميل Dynamics 365 for Operations.
2.  انقر فوق **البيع بالتجزئة والتجارة** &gt; **إعداد المقر الرئيسي** &gt; **المعلمات** &gt; **معلمات البيع بالتجزئة**.
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

بالإضافة إلى ذلك، يتم تمكين التسجيل المتعلق بصناعة بطاقات الدفع (PCI) لقاعدة بيانات Dynamics 365 for Operations. **ملاحظة:** هناك خيار لتكوين مجدول البيع بالتجزئة بشكل منفصل. يتيح لك هذا الخيار إعادة تعيين تكوين مجدول البيع بالتجزئة إلى الإعدادات الافتراضية الخاصة به. وبعد إتمام عملية التهيئة، يجب عليك تكوين البيانات الإضافية للبيع بالتجزئة. فيما يلي بعض الأمثلة:

-   معلمات البيع بالتجزئة
-   معلمات مجدول البيع بالتجزئة
-   قنوات البيع بالتجزئة
-   السجلات والأجهزة
-   عمليات الفرز




