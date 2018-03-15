--- 
title: " تكوين توصيات المنتجات المدعومة بنظام التعلم الآلي"
description: "يقوم هذا الإجراء بتحديث البيانات في مخزن الكيانات المستخدم من قبل نظام التعلم الآلي الذي يدعم التوصيات، ثم يمكّن توصيات المنتجات على عملاء نقطة البيع."
author: ashishmsft
manager: AnnBe
ms.date: 10/27/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations, Retail
ms.search.region: Global
ms.search.industry: Retail
ms.author: asharchw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: ea07d8e91c94d9fdad4c2d05533981e254420188
ms.openlocfilehash: 277ffb879b80fe57deeaa2b52c1543baaf820274
ms.contentlocale: ar-sa
ms.lasthandoff: 02/07/2018

---
# <a name="configure-machine-learning-powered-product-recommendations"></a><span data-ttu-id="28fb4-103"> تكوين توصيات المنتجات المدعومة بنظام التعلم الآلي</span><span class="sxs-lookup"><span data-stu-id="28fb4-103">Configure machine learning-powered product recommendations</span></span>

[!include[task guide banner](../includes/task-guide-banner.md)]

<span data-ttu-id="28fb4-104">يقوم هذا الإجراء بتحديث البيانات في مخزن الكيانات المستخدم من قبل نظام التعلم الآلي الذي يدعم التوصيات، ثم يمكّن توصيات المنتجات على عملاء نقطة البيع.</span><span class="sxs-lookup"><span data-stu-id="28fb4-104">This procedure refreshes the data in the Entity store that is used by the machine learning system that powers product recommendations, and then enables product recommendations on POS clients.</span></span> <span data-ttu-id="28fb4-105">ويستخدم هذا الإجراء شركة USRT في بيانات العرض التوضيحي.</span><span class="sxs-lookup"><span data-stu-id="28fb4-105">This procedure uses the USRT company in demo data.</span></span>

1. <span data-ttu-id="28fb4-106">انتقل إلى إدارة النظام > الإعداد > متجر الكيانات‬.</span><span class="sxs-lookup"><span data-stu-id="28fb4-106">Go to System administration > Setup > Entity Store.</span></span>
2. <span data-ttu-id="28fb4-107">في القائمة، ابحث عن السجل "RetailSales" وحدده.</span><span class="sxs-lookup"><span data-stu-id="28fb4-107">In the list, find and select the record 'RetailSales'.</span></span>
3. <span data-ttu-id="28fb4-108">انقر فوق "تحديث".</span><span class="sxs-lookup"><span data-stu-id="28fb4-108">Click Refresh.</span></span>
4. <span data-ttu-id="28fb4-109">انقر فوق "موافق".</span><span class="sxs-lookup"><span data-stu-id="28fb4-109">Click OK.</span></span>
5. <span data-ttu-id="28fb4-110">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="28fb4-110">Close the page.</span></span>
6. <span data-ttu-id="28fb4-111">انتقل إلى البيع بالتجزئة والتجارة > إعداد المراكز الرئيسية > المعلمات > معلمات البيع بالتجزئة‬.</span><span class="sxs-lookup"><span data-stu-id="28fb4-111">Go to Retail and commerce > Headquarters setup > Parameters > Retail parameters.</span></span>
7. <span data-ttu-id="28fb4-112">انقر فوق علامة التبويب "التعلم الآلي".</span><span class="sxs-lookup"><span data-stu-id="28fb4-112">Click the Machine learning tab.</span></span>
8. <span data-ttu-id="28fb4-113">حدد "نعم" في حقل "تمكين توصيات المنتجات‬".</span><span class="sxs-lookup"><span data-stu-id="28fb4-113">Select 'Yes' in the Enable product recommendations field.</span></span>
    * <span data-ttu-id="28fb4-114">إذا تلقيت الرسالة "تعذر استرداد نماذج التوصية"، فسبب ذلك يعود إلى تحديث مخزن الكيانات مؤخرًا دون أن ينتهي النظام من استيعاب البيانات الجديدة.</span><span class="sxs-lookup"><span data-stu-id="28fb4-114">If you receive the message "The recommendation models couldn't be retrieved", it’s because you refreshed the Entity Store very recently and the system may not have finished assimilating the new data.</span></span> <span data-ttu-id="28fb4-115">انتظر من ساعتين إلى ثلاث ساعات وحاول مرة أخرى.</span><span class="sxs-lookup"><span data-stu-id="28fb4-115">Wait 2-3 hours and try again.</span></span>  
9. <span data-ttu-id="28fb4-116">انقر فوق "حفظ".</span><span class="sxs-lookup"><span data-stu-id="28fb4-116">Click Save.</span></span>
10. <span data-ttu-id="28fb4-117">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="28fb4-117">Close the page.</span></span>


