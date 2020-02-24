---
title: تكوين المعلمات التي تؤثر على كشوف البيع بالتجزئة
description: يوضح هذا الموضوع تكوينات معلمات Commerce التي تؤثر على كيفية إنشاء كشوفات الحساب وترحيلها.
author: josaw1
manager: AnnBe
ms.date: 08/01/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: RetailParameters
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: d8cae6d2fa7c469f50fa92141a6cb5a0af1df4b0
ms.sourcegitcommit: 81a647904dd305c4be2e4b683689f128548a872d
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 02/01/2020
ms.locfileid: "3021467"
---
# <a name="configure-parameters-that-affect-retail-statements"></a><span data-ttu-id="591e5-103">تكوين المعلمات التي تؤثر على كشوف البيع بالتجزئة</span><span class="sxs-lookup"><span data-stu-id="591e5-103">Configure parameters that affect retail statements</span></span>

[!include[task guide banner](../includes/task-guide-banner.md)]

<span data-ttu-id="591e5-104">يوضح هذا الموضوع تكوينات معلمات Commerce التي تؤثر على كيفية إنشاء كشوفات الحساب وترحيلها.</span><span class="sxs-lookup"><span data-stu-id="591e5-104">This topic demonstrates configurations for Commerce parameters that affect how statements get created and posted.</span></span> <span data-ttu-id="591e5-105">يستخدم هذا الإجراء شركة بيانات العرض التوضيحي USRT.</span><span class="sxs-lookup"><span data-stu-id="591e5-105">This procedure uses the USRT demo company.</span></span>

1. <span data-ttu-id="591e5-106">في جزء التنقل، انتقل إلى **الوحدات > Retail and Commerce > إعداد المراكز الرئيسية ‬ > المعلمات > معلمات Commerce‬**.</span><span class="sxs-lookup"><span data-stu-id="591e5-106">In the navigation pane, go to **Modules > Retail and Commerce > Headquarters setup  > Parameters > Commerce parameters**.</span></span>
2. <span data-ttu-id="591e5-107">حدد علامة تبويب **الترحيل**.</span><span class="sxs-lookup"><span data-stu-id="591e5-107">Select the **Posting** tab.</span></span>
    - <span data-ttu-id="591e5-108">حدد **نعم** إذا أردت تريد ترحيل مبالغ الخصم الدوري على وجه التحديد.</span><span class="sxs-lookup"><span data-stu-id="591e5-108">Select **Yes** if you want to post the periodic discount amounts specifically.</span></span>  
    - <span data-ttu-id="591e5-109">حدد **قياسي** لاستخدام الحسابات الافتراضية، أو حدد **دوري** إذا كنت تريد تحديد الحساب المراد استخدامه لكل خصم دوري.</span><span class="sxs-lookup"><span data-stu-id="591e5-109">Select **Standard** to use default accounts, or select **Periodic** if you want to define which account to use for each periodic discount.</span></span>  
      - <span data-ttu-id="591e5-110">حدد **الملخص** إذا كان ينبغي تجميع بنود المخزون كلما كان ذلك ممكنًا.</span><span class="sxs-lookup"><span data-stu-id="591e5-110">Select **Summary** if inventory lines should get aggregated whenever possible.</span></span>  
      - <span data-ttu-id="591e5-111">حدد **نعم** إذا كان ينبغي تسوية الفواتير والمدفوعات تلقائيًا كجزء من عملية ترحيل كشف الحساب.</span><span class="sxs-lookup"><span data-stu-id="591e5-111">Select **Yes** if Invoices and Payments should get automatically settled as part of the Statement posting process.</span></span>  
      - <span data-ttu-id="591e5-112">حدد **نعم** إذا كان ينبغي تجميع حركات الإيداع بالخزينة.</span><span class="sxs-lookup"><span data-stu-id="591e5-112">Select **Yes** if Safe drop transactions should get aggregated.</span></span>  
      - <span data-ttu-id="591e5-113">حدد **نعم** إذا كان ينبغي تجميع حركات الإيداع البنكي.</span><span class="sxs-lookup"><span data-stu-id="591e5-113">Select **Yes** if Bank drop transactions should get aggregated.</span></span>  
      - <span data-ttu-id="591e5-114">حدد **نعم** لتشغيل التجميع لترحيل كشف الحساب.</span><span class="sxs-lookup"><span data-stu-id="591e5-114">Select **Yes** to turn aggregation on for Statement posting.</span></span>  
      - <span data-ttu-id="591e5-115">حدد **نعم** لإنشاء الأوامر ومعالجتها بالتوازي عند ترحيل كشوفات الحساب.</span><span class="sxs-lookup"><span data-stu-id="591e5-115">Select **Yes** to create and process orders in parallel when statements are posted.</span></span>  
      - <span data-ttu-id="591e5-116">أدخل الحد الأقصى للأوامر التي سيتم معالجتها في كل مهمة وظيفة دفعية.</span><span class="sxs-lookup"><span data-stu-id="591e5-116">Enter the maximum orders to be processed in each batch job task.</span></span>  
3. <span data-ttu-id="591e5-117">حدد **حفظ**.</span><span class="sxs-lookup"><span data-stu-id="591e5-117">Select **Save**.</span></span>

