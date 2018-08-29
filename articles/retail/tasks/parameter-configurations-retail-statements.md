--- 
title: "تكوين معلمات البيع بالتجزئة التي تؤثر على كشوف حسابات البيع بالتجزئة"
description: "يوضح هذا الإجراء تكوينات لمعلمات البيع بالتجزئة التي تؤثر على كيفية إنشاء كشوفات حساب البيع بالتجزئة وترحيلها."
author: josaw1
manager: AnnBe
ms.date: 11/14/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations, Retail
ms.search.region: Global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 5098fb3339403b6f2779dfe3bb7ef5c4ca78051f
ms.openlocfilehash: ff12587d8332801131d5b0cac84e0db38f8f6142
ms.contentlocale: ar-sa
ms.lasthandoff: 08/08/2018

---
# <a name="configure-retail-parameters-that-affect-retail-statements"></a><span data-ttu-id="fe17b-103">تكوين معلمات البيع بالتجزئة التي تؤثر على كشوف حسابات البيع بالتجزئة</span><span class="sxs-lookup"><span data-stu-id="fe17b-103">Configure Retail parameters that affect retail statements</span></span>

[!include [task guide banner](../includes/task-guide-banner.md)]

<span data-ttu-id="fe17b-104">يوضح هذا الإجراء تكوينات لمعلمات البيع بالتجزئة التي تؤثر على كيفية إنشاء كشوفات حساب البيع بالتجزئة وترحيلها.</span><span class="sxs-lookup"><span data-stu-id="fe17b-104">This procedure demonstrates configurations for Retail parameters that affect how Retail statements get created and posted.</span></span> <span data-ttu-id="fe17b-105">يستخدم هذا الإجراء شركة بيانات العرض التوضيحي USRT.</span><span class="sxs-lookup"><span data-stu-id="fe17b-105">This procedure uses the USRT demo company.</span></span>

1. <span data-ttu-id="fe17b-106">انتقل إلى البيع بالتجزئة والتجارة > إعداد المراكز الرئيسية > المعلمات > معلمات البيع بالتجزئة‬.</span><span class="sxs-lookup"><span data-stu-id="fe17b-106">Go to Retail and commerce > Headquarters setup  > Parameters > Retail parameters.</span></span>
2. <span data-ttu-id="fe17b-107">انقر فوق علامة التبويب ترحيل.</span><span class="sxs-lookup"><span data-stu-id="fe17b-107">Click the Posting tab.</span></span>
    * <span data-ttu-id="fe17b-108">حدد "نعم" إذا كنت تريد ترحيل مبالغ الخصم الدوري على وجه التحديد.</span><span class="sxs-lookup"><span data-stu-id="fe17b-108">Select "Yes" if you want to post the periodic discount amounts specifically.</span></span>  
    * <span data-ttu-id="fe17b-109">حدد "المعايير" لاستخدام الحسابات الافتراضية، أو حدد "دوري" إذا كنت تريد تحديد الحساب المراد استخدامه لكل خصم دوري.</span><span class="sxs-lookup"><span data-stu-id="fe17b-109">Select "Standard" to use default accounts, or select "Periodic" if you want to define which account to use for each periodic discount.</span></span>  
    * <span data-ttu-id="fe17b-110">حدد "الملخص" إذا كان ينبغي تجميع بنود المخزون كلما كان ذلك ممكنًا.</span><span class="sxs-lookup"><span data-stu-id="fe17b-110">Select "Summary" if inventory lines should get aggregated whenever possible.</span></span>  
    * <span data-ttu-id="fe17b-111">حدد "نعم" إذا كان ينبغي تسوية الفواتير والمدفوعات تلقائيًا كجزء من عملية ترحيل كشف الحساب.</span><span class="sxs-lookup"><span data-stu-id="fe17b-111">Select "Yes" if Invoices and Payments should get automatically settled as part of the Statement posting process.</span></span>  
    * <span data-ttu-id="fe17b-112">حدد "نعم" إذا كان ينبغي تجميع حركات الإيداع بالخزينة.</span><span class="sxs-lookup"><span data-stu-id="fe17b-112">Select "Yes" if Safe drop transactions should get aggregated.</span></span>  
    * <span data-ttu-id="fe17b-113">حدد "نعم" إذا كان ينبغي تجميع حركات الإيداع البنكي.</span><span class="sxs-lookup"><span data-stu-id="fe17b-113">Select "Yes" if Bank drop transactions should get aggregated.</span></span>  
    * <span data-ttu-id="fe17b-114">حدد "نعم" لتشغيل التجميع لترحيل كشف الحساب.</span><span class="sxs-lookup"><span data-stu-id="fe17b-114">Select "Yes" to turn aggregation on for Statement posting.</span></span>  
    * <span data-ttu-id="fe17b-115">حدد "نعم" لإنشاء الأوامر ومعالجتها بالتوازي عند ترحيل كشوفات الحساب.</span><span class="sxs-lookup"><span data-stu-id="fe17b-115">Select "Yes" to create and process orders in parallel when statements are posted.</span></span>  
    * <span data-ttu-id="fe17b-116">أدخل الحد الأقصى للأوامر التي سيتم معالجتها في كل مهمة وظيفة دفعية.</span><span class="sxs-lookup"><span data-stu-id="fe17b-116">Enter the maximum orders to be processed in each batch job task.</span></span>  
3. <span data-ttu-id="fe17b-117">انقر فوق "حفظ".</span><span class="sxs-lookup"><span data-stu-id="fe17b-117">Click Save.</span></span>


