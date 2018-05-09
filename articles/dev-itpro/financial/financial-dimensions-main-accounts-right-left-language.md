---
title: "الأبعاد المالية والحسابات الرئيسية بلغة تكتب من اليمين إلى اليسار"
description: "يصف هذا الموضوع بعض قرارات التنفيذ التي ينبغي وضعها في الاعتبار عند استخدام لغة ذات اتجاه من اليمين إلى اليسار، ويجب إعداد الأبعاد المالية والحسابات الرئيسية."
author: aprilolson
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.custom: 222564
ms.assetid: 875dcebb-1bbb-4841-a8c6-9e134da07e96
ms.search.region: global
ms.author: aolson
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: 857f2c7ea948717695c3c741a20f6b3e922b33e1
ms.contentlocale: ar-sa
ms.lasthandoff: 05/08/2018

---

# <a name="financial-dimensions-and-main-accounts-in-a-right-to-left-language"></a><span data-ttu-id="d7ee3-103">الأبعاد المالية والحسابات الرئيسية بلغة تكتب من اليمين إلى اليسار</span><span class="sxs-lookup"><span data-stu-id="d7ee3-103">Financial dimensions and main accounts in a right-to-left language</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="d7ee3-104">يصف هذا الموضوع بعض قرارات التنفيذ التي ينبغي وضعها في الاعتبار عند استخدام لغة ذات اتجاه من اليمين إلى اليسار، ويجب إعداد الأبعاد المالية والحسابات الرئيسية.</span><span class="sxs-lookup"><span data-stu-id="d7ee3-104">This topic describes some of the implementation decisions that you should consider when you use a right-to-left language, and you must set up financial dimensions and main accounts.</span></span>

<span data-ttu-id="d7ee3-105">تُعد الأبعاد المالية والحسابات الرئيسية مكونات أساسية من مرحلة التخطيط في عملية التنفيذ.</span><span class="sxs-lookup"><span data-stu-id="d7ee3-105">Financial dimensions and main accounts are key components of the planning phase for an implementation.</span></span> <span data-ttu-id="d7ee3-106">يتم استخدام الأبعاد المالية والحسابات الرئيسية، بعد إنشائها في النظام، في الصفحات **تكوين بنيات حساب** و**بُنى قاعدة متقدمة‬** و**تكوين الأبعاد المالية لتكامل التطبيقات‬**.</span><span class="sxs-lookup"><span data-stu-id="d7ee3-106">After financial dimensions and main accounts are created in the system, they are used on the **Configure account structures**, **Advanced rule structures**, and **Financial dimension configuration for integrating applications** pages.</span></span> <span data-ttu-id="d7ee3-107">يتم استخدام الترتيب الذي تم تحديده في تلك الصفحات في النظام لإدخال واستهلاك البيانات.</span><span class="sxs-lookup"><span data-stu-id="d7ee3-107">The order that is defined on those pages is used in the system for data entry and consumption.</span></span> <span data-ttu-id="d7ee3-108">في بعض الأماكن في النظام، تظهر الأبعاد المالية والحسابات الرئيسية في حقول منفصلة.</span><span class="sxs-lookup"><span data-stu-id="d7ee3-108">In some places in the system, the financial dimensions and main accounts appear in separate fields.</span></span> <span data-ttu-id="d7ee3-109">ولكن الأبعاد المالية والحسابات الرئيسية تظهر في أماكن أخرى، مثل دفاتر اليومية، كسلسلة واحدة.</span><span class="sxs-lookup"><span data-stu-id="d7ee3-109">However, in other places, such as journals, the financial dimensions and main accounts appear as a single string.</span></span>

### <a name="best-practices-for-setting-up-financial-dimensions-and-main-accounts-in-a-right-to-left-system"></a><span data-ttu-id="d7ee3-110">أفضل الممارسات لإعداد الأبعاد المالية والحسابات الرئيسية في نظام من اليمين لليسار</span><span class="sxs-lookup"><span data-stu-id="d7ee3-110">Best practices for setting up financial dimensions and main accounts in a right-to-left system</span></span>

-   <span data-ttu-id="d7ee3-111">عندما تعيّن محددًا لأدلة الحسابات، حدد أحد خيارات المحددات المزدوجة: واصلة مزدوجة (--) أو شريط مزدوج (||) أو نقطة مزدوجة (..) أو شرطة سفلية مزدوجة (\_\_).</span><span class="sxs-lookup"><span data-stu-id="d7ee3-111">When you select the delimiter for charts of accounts, select one of the double delimiter options: double hyphen (--), double bar (||) or double period (..), or double underscore (\_\_).</span></span>
-   <span data-ttu-id="d7ee3-112">عندما تنشئ قيم الحسابات الرئيسية والأبعاد المالية، استخدم فقط الأرقام وأحرف اللغة من اليمين إلى اليسار.</span><span class="sxs-lookup"><span data-stu-id="d7ee3-112">When you create financial dimension and main account values, use only numbers and right-to-left language characters.</span></span>
-   <span data-ttu-id="d7ee3-113">تجنب استخدام محدد دليل الحسابات المحدد في قيم الأبعاد المالية والحسابات الرئيسية.</span><span class="sxs-lookup"><span data-stu-id="d7ee3-113">Avoid using the selected chart of accounts delimiter in financial dimension and main account values.</span></span>

<span data-ttu-id="d7ee3-114">يساعدك اتباع هذه الممارسات على ضمان التمثيل المتسق للترتيب المعرّف من قِبل المستخدم عبر النظام.</span><span class="sxs-lookup"><span data-stu-id="d7ee3-114">By following these best practices, you help guarantee consistent representation of the user defined-order throughout the system.</span></span>




