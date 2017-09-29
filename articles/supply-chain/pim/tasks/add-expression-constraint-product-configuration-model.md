--- 
title: "إضافة قيد تعبير إلى نموذج تكوين منتج"
description: "يوضح هذا الإجراء كيفية إضافة تعبير قيد جديد إلى نموذج تكوين منتج."
author: YuyuScheller
manager: AnnBe
ms.date: 10/27/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Operations
ms.search.region: Global
ms.author: yuyus
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: 8db46c5b8361c96745b440c0d0684e18c06a6c6f
ms.contentlocale: ar-sa
ms.lasthandoff: 08/29/2017

---
# <a name="add-an-expression-constraint-to-a-product-configuration-model"></a><span data-ttu-id="2c0fb-103">إضافة قيد تعبير إلى نموذج تكوين منتج</span><span class="sxs-lookup"><span data-stu-id="2c0fb-103">Add an expression constraint to a product configuration model</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="2c0fb-104">يوضح هذا الإجراء كيفية إضافة تعبير قيد جديد إلى نموذج تكوين منتج.</span><span class="sxs-lookup"><span data-stu-id="2c0fb-104">This procedure shows how you can add a new constraint expression to a product configuration model.</span></span> <span data-ttu-id="2c0fb-105">ويُظهر كيفية إصدار أمر رسمي بوجوب يجب تطبيق حماية الزاوية على مكبر صوت إذا قام المستخدم بتحديد شبكة أمامية معدنية.</span><span class="sxs-lookup"><span data-stu-id="2c0fb-105">It shows how you can mandate that corner protection must be applied to a speaker if the user has selected a front grill in metal.</span></span> <span data-ttu-id="2c0fb-106">يستخدم الإجراء المكون مكبر الصوت المتطور في شركة العرض التوضيحي USMF.</span><span class="sxs-lookup"><span data-stu-id="2c0fb-106">The procedure uses the High end speaker component in the demo company USMF.</span></span>


## <a name="create-an-expression-constraint"></a><span data-ttu-id="2c0fb-107">قم بإنشاء قيد تعبير</span><span class="sxs-lookup"><span data-stu-id="2c0fb-107">Create an expression constraint</span></span>
1. <span data-ttu-id="2c0fb-108">انقر فوق "تعريف نموذج متغير المنتج"ز</span><span class="sxs-lookup"><span data-stu-id="2c0fb-108">Click Product variant model definition.</span></span>
2. <span data-ttu-id="2c0fb-109">انقر فوق "نماذج تكوين المنتجات".</span><span class="sxs-lookup"><span data-stu-id="2c0fb-109">Click Product configuration models.</span></span>
3. <span data-ttu-id="2c0fb-110">في القائمة، قم بالبحث عن السجل المطلوب وحدده.</span><span class="sxs-lookup"><span data-stu-id="2c0fb-110">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="2c0fb-111">يستخدم هذا المثال نموذج مكبر الصوت المتطور.</span><span class="sxs-lookup"><span data-stu-id="2c0fb-111">This example uses the high end speaker model.</span></span>  
4. <span data-ttu-id="2c0fb-112">في القائمة، انقر فوق الارتباط في الصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="2c0fb-112">In the list, click the link in the selected row.</span></span>
5. <span data-ttu-id="2c0fb-113">قم بتوسيع القسم "القيود".</span><span class="sxs-lookup"><span data-stu-id="2c0fb-113">Expand the Constraints section.</span></span>
6. <span data-ttu-id="2c0fb-114">وانقر فوق إضافة.</span><span class="sxs-lookup"><span data-stu-id="2c0fb-114">Click Add.</span></span>
7. <span data-ttu-id="2c0fb-115">انقر فوق "إنشاء".</span><span class="sxs-lookup"><span data-stu-id="2c0fb-115">Click Create.</span></span>
8. <span data-ttu-id="2c0fb-116">في حقل "الاسم"، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="2c0fb-116">In the Name field, type a value.</span></span>

## <a name="enter-expression"></a><span data-ttu-id="2c0fb-117">إدخال تعبير</span><span class="sxs-lookup"><span data-stu-id="2c0fb-117">Enter expression</span></span>
1. <span data-ttu-id="2c0fb-118">انقر فوق "تحرير التعبير".</span><span class="sxs-lookup"><span data-stu-id="2c0fb-118">Click Edit expression.</span></span>
    * <span data-ttu-id="2c0fb-119">إذا قمت بإلغاء تأمين واجهة المستخدم في تسجيل المهمة في هذه المرحلة، يمكنك استخدام IntelliSense وقائمة من الرموز لإنشاء تعبير القيد.</span><span class="sxs-lookup"><span data-stu-id="2c0fb-119">If you unlock the user interface in the task recording at this stage, you can use IntelliSense and the list of symbols to build the constraint expression .</span></span>  
2. <span data-ttu-id="2c0fb-120">في الحقل "ConstraintBody"، أدخل "Implies[FrontGrill=="Metal", CornerProtection]".</span><span class="sxs-lookup"><span data-stu-id="2c0fb-120">In the ConstraintBody field, enter 'Implies[FrontGrill=="Metal", CornerProtection] '.</span></span>
    * <span data-ttu-id="2c0fb-121">يوضح منطق التعبير هذا: إذا كانت الشبكة الأمامية معدنية، فيجب تحديد خيار حماية الزاوية.</span><span class="sxs-lookup"><span data-stu-id="2c0fb-121">This expression logic states: If the Front grill is  metal, then the corner protection option must be selected.</span></span>  
3. <span data-ttu-id="2c0fb-122">انقر فوق "التحقق من الصحة‬".</span><span class="sxs-lookup"><span data-stu-id="2c0fb-122">Click Validate.</span></span>
    * <span data-ttu-id="2c0fb-123">يتم تشغيل دالة التحقق من الصحة من خلال تعبير القيد وتتحقق من وجود أخطاء في بناء الجملة.</span><span class="sxs-lookup"><span data-stu-id="2c0fb-123">The validate function runs through the constraint expression and checks for syntax errors.</span></span>  
4. <span data-ttu-id="2c0fb-124">انقر فوق "إغلاق".</span><span class="sxs-lookup"><span data-stu-id="2c0fb-124">Click Close.</span></span>
5. <span data-ttu-id="2c0fb-125">انقر فوق "موافق".</span><span class="sxs-lookup"><span data-stu-id="2c0fb-125">Click OK.</span></span>


