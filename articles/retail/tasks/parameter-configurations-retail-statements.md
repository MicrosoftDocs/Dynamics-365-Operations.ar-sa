--- 
title: " تكوينات المعلمة لبيانات البيع بالتجزئة"
description: "يوضح هذا الإجراء تكوينات لمعلمات البيع بالتجزئة التي تؤثر على كيفية إنشاء كشوفات حساب البيع بالتجزئة وترحيلها."
author: josaw1
manager: AnnBe
ms.date: 11/14/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: 731a3ec06efa103ba663df83240c77dfe78bb7cd
ms.contentlocale: ar-sa
ms.lasthandoff: 08/29/2017

---
# <a name="parameter-configurations-for-retail-statements"></a><span data-ttu-id="e193f-103"> تكوينات المعلمة لبيانات البيع بالتجزئة</span><span class="sxs-lookup"><span data-stu-id="e193f-103">Parameter configurations for Retail statements</span></span>

[!include[task guide banner](../includes/task-guide-banner.md)]

<span data-ttu-id="e193f-104">يوضح هذا الإجراء تكوينات لمعلمات البيع بالتجزئة التي تؤثر على كيفية إنشاء كشوفات حساب البيع بالتجزئة وترحيلها.</span><span class="sxs-lookup"><span data-stu-id="e193f-104">This procedure demonstrates configurations for Retail parameters that affect how Retail statements get created and posted.</span></span> <span data-ttu-id="e193f-105">يستخدم هذا الإجراء شركة بيانات العرض التوضيحي USRT.</span><span class="sxs-lookup"><span data-stu-id="e193f-105">This procedure uses the USRT demo company.</span></span>

1. <span data-ttu-id="e193f-106">انتقل إلى البيع بالتجزئة والتجارة > إعداد المراكز الرئيسية > المعلمات > معلمات البيع بالتجزئة‬.</span><span class="sxs-lookup"><span data-stu-id="e193f-106">Go to Retail and commerce > Headquarters setup  > Parameters > Retail parameters.</span></span>
2. <span data-ttu-id="e193f-107">انقر فوق علامة التبويب ترحيل.</span><span class="sxs-lookup"><span data-stu-id="e193f-107">Click the Posting tab.</span></span>
    * <span data-ttu-id="e193f-108">حدد "نعم" إذا كنت تريد ترحيل مبالغ الخصم الدوري على وجه التحديد.</span><span class="sxs-lookup"><span data-stu-id="e193f-108">Select "Yes" if you want to post the periodic discount amounts specifically.</span></span>  
    * <span data-ttu-id="e193f-109">حدد "المعايير" لاستخدام الحسابات الافتراضية، أو حدد "دوري" إذا كنت تريد تحديد الحساب المراد استخدامه لكل خصم دوري.</span><span class="sxs-lookup"><span data-stu-id="e193f-109">Select "Standard" to use default accounts, or select "Periodic" if you want to define which account to use for each periodic discount.</span></span>  
    * <span data-ttu-id="e193f-110">حدد "الملخص" إذا كان ينبغي تجميع بنود المخزون كلما كان ذلك ممكنًا.</span><span class="sxs-lookup"><span data-stu-id="e193f-110">Select "Summary" if inventory lines should get aggregated whenever possible.</span></span>  
    * <span data-ttu-id="e193f-111">حدد "نعم" إذا كان ينبغي تسوية الفواتير والمدفوعات تلقائيًا كجزء من عملية ترحيل كشف الحساب.</span><span class="sxs-lookup"><span data-stu-id="e193f-111">Select "Yes" if Invoices and Payments should get automatically settled as part of the Statement posting process.</span></span>  
    * <span data-ttu-id="e193f-112">حدد "نعم" إذا كان ينبغي تجميع حركات الإيداع بالخزينة.</span><span class="sxs-lookup"><span data-stu-id="e193f-112">Select "Yes" if Safe drop transactions should get aggregated.</span></span>  
    * <span data-ttu-id="e193f-113">حدد "نعم" إذا كان ينبغي تجميع حركات الإيداع البنكي.</span><span class="sxs-lookup"><span data-stu-id="e193f-113">Select "Yes" if Bank drop transactions should get aggregated.</span></span>  
    * <span data-ttu-id="e193f-114">حدد "نعم" لتشغيل التجميع لترحيل كشف الحساب.</span><span class="sxs-lookup"><span data-stu-id="e193f-114">Select "Yes" to turn aggregation on for Statement posting.</span></span>  
    * <span data-ttu-id="e193f-115">حدد "نعم" لإنشاء الأوامر ومعالجتها بالتوازي عند ترحيل كشوفات الحساب.</span><span class="sxs-lookup"><span data-stu-id="e193f-115">Select "Yes" to create and process orders in parallel when statements are posted.</span></span>  
    * <span data-ttu-id="e193f-116">أدخل الحد الأقصى للأوامر التي سيتم معالجتها في كل مهمة وظيفة دفعية.</span><span class="sxs-lookup"><span data-stu-id="e193f-116">Enter the maximum orders to be processed in each batch job task.</span></span>  
3. <span data-ttu-id="e193f-117">انقر فوق "حفظ".</span><span class="sxs-lookup"><span data-stu-id="e193f-117">Click Save.</span></span>


