---
title: "تكوين قرار شرطي في سير عمل‬"
description: "استخدم الإجراء التالي لتكوين خصائص قرار شرطي."
author: sericks007
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User, IT Pro
ms.reviewer: sericks
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 195703
ms.assetid: cd5554a4-210c-4c20-a7d3-4b1563c2b5df
ms.search.region: Global
ms.author: donaldc
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: e9d5c8add546cad0446e863f64cac8f9cb603cbb
ms.contentlocale: ar-sa
ms.lasthandoff: 09/29/2017

---

# <a name="configure-a-conditional-decision-in-a-workflow"></a><span data-ttu-id="b85f9-103">تكوين قرار شرطي في سير عمل‬</span><span class="sxs-lookup"><span data-stu-id="b85f9-103">Configure a conditional decision in a workflow</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="b85f9-104">استخدم الإجراء التالي لتكوين خصائص قرار شرطي.</span><span class="sxs-lookup"><span data-stu-id="b85f9-104">Use the following procedure to configure the properties of a conditional decision.</span></span>

<span data-ttu-id="b85f9-105">القرار المشروط هو نقطة يتفرع عندها سير العمل إلى فرعين.</span><span class="sxs-lookup"><span data-stu-id="b85f9-105">A conditional decision is a point at which a workflow divides into two branches.</span></span> <span data-ttu-id="b85f9-106">لتكوين قرار شرطي، في محرر سير العمل، انقر بزر الماوس الأيمن فوق القرار الشرطي، ثم انقر فوق **خصائص** لفتح النموذج **خصائص**.</span><span class="sxs-lookup"><span data-stu-id="b85f9-106">To configure a conditional decision, in the workflow editor, right-click the conditional decision, and then click **Properties** to open the **Properties** form.</span></span>

## <a name="name-a-decision"></a><span data-ttu-id="b85f9-107">تسمية قرار</span><span class="sxs-lookup"><span data-stu-id="b85f9-107">Name a decision</span></span>
<span data-ttu-id="b85f9-108">اتبع الخطوات التالية لإدخال اسم للقرار الشرطي.</span><span class="sxs-lookup"><span data-stu-id="b85f9-108">Follow these steps to enter a name for a conditional decision.</span></span>
1.  <span data-ttu-id="b85f9-109">في الجزء الأيمن، انقر فوق **الإعدادات الأساسية‬**.</span><span class="sxs-lookup"><span data-stu-id="b85f9-109">In the left pane, click **Basic Settings**.</span></span>
2.  <span data-ttu-id="b85f9-110">في حقل **الاسم**، أدخل اسمًا فريدًا للقرار الشرطي.</span><span class="sxs-lookup"><span data-stu-id="b85f9-110">In the **Name** field, enter a unique name for the conditional decision.</span></span>

## <a name="set-conditions"></a><span data-ttu-id="b85f9-111"> تعيين الشروط</span><span class="sxs-lookup"><span data-stu-id="b85f9-111">Set conditions</span></span>
<span data-ttu-id="b85f9-112">يحدد النظام العلامة التجارية التي يجب استخدامها عن طريق تقييم المستند المرسل لتحديد ما إذا كان يستوفي شروطًا معينة.</span><span class="sxs-lookup"><span data-stu-id="b85f9-112">The system determines which branch is used by evaluating the submitted document to determine whether it meets specific conditions.</span></span>
1.  <span data-ttu-id="b85f9-113">في الجزء الأيمن، انقر فوق **الإعدادات الأساسية‬**.</span><span class="sxs-lookup"><span data-stu-id="b85f9-113">In the left pane, click **Basic Settings**.</span></span>
2.  <span data-ttu-id="b85f9-114">انقر فوق **إضافة شرط**.</span><span class="sxs-lookup"><span data-stu-id="b85f9-114">Click **Add condition**.</span></span>
3.  <span data-ttu-id="b85f9-115">يتيح إمكانية إدخال شرط.</span><span class="sxs-lookup"><span data-stu-id="b85f9-115">Enter a condition.</span></span>
4.  <span data-ttu-id="b85f9-116">أدخل الشروط الإضافية، إذا كانت مطلوبة.</span><span class="sxs-lookup"><span data-stu-id="b85f9-116">Enter additional conditions, if they are required.</span></span>
5.  <span data-ttu-id="b85f9-117">للتأكد من تكوين الشروط التي قمت بإدخالها بشكل صحيح، أكمل الخطوات التالية:</span><span class="sxs-lookup"><span data-stu-id="b85f9-117">To verify that the conditions that you entered are configured correctly, complete the following steps:</span></span>
    1.  <span data-ttu-id="b85f9-118">انقر فوق **اختبار** لفتح النموذج **اختبار حالة سير العمل**.</span><span class="sxs-lookup"><span data-stu-id="b85f9-118">Click **Test** to open the **Test workflow condition** form.</span></span>
    2.  <span data-ttu-id="b85f9-119">حدد سجلاً في المنطقة **‏‏التحقق من الشرط** من النموذج.</span><span class="sxs-lookup"><span data-stu-id="b85f9-119">Select a record in the **Validate condition** area of the form.</span></span>
    3.  <span data-ttu-id="b85f9-120">انقر فوق **اختبار**.</span><span class="sxs-lookup"><span data-stu-id="b85f9-120">Click **Test**.</span></span> <span data-ttu-id="b85f9-121">سيقوم النظام بتقييم السجل لمعرفة ما إذا كان يستوفي الشروط التي قمت بتحديدها أم لا.</span><span class="sxs-lookup"><span data-stu-id="b85f9-121">The system evaluates the record to determine whether it meets the conditions that you defined.</span></span>
    4.  <span data-ttu-id="b85f9-122">انقر فوق **موافق** أو **إلغاء الأمر** للعودة إلى النموذج **خصائص**.</span><span class="sxs-lookup"><span data-stu-id="b85f9-122">Click **OK** or **Cancel** to return to the **Properties** form.</span></span>






