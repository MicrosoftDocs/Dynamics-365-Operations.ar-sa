---
title: إضافة قيد تعبير إلى نموذج تكوين منتج
description: يوضح هذا الإجراء كيفية إضافة تعبير قيد جديد إلى نموذج تكوين منتج.
author: ShylaThompson
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: DefaultDashboard, EcoResProductVariantMaintainWorkspace, PCProductConfigurationModelListPage, PCProductConfigurationModelDetails, SysClientPolymorphicCreateSelector, PCConstraintEditor, PCRuntimeConfiguratorValidate
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 9cd5475e48cbcd8dcee6b228297f58e364ac503d
ms.sourcegitcommit: fa99a36c3d30d0c0577fd3f63ed6bf2f71599e40
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 04/20/2021
ms.locfileid: "5920871"
---
# <a name="add-an-expression-constraint-to-a-product-configuration-model"></a><span data-ttu-id="95553-103">إضافة قيد تعبير إلى نموذج تكوين منتج</span><span class="sxs-lookup"><span data-stu-id="95553-103">Add an expression constraint to a product configuration model</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="95553-104">يوضح هذا الإجراء كيفية إضافة تعبير قيد جديد إلى نموذج تكوين منتج.</span><span class="sxs-lookup"><span data-stu-id="95553-104">This procedure shows how you can add a new constraint expression to a product configuration model.</span></span> <span data-ttu-id="95553-105">ويُظهر كيفية إصدار أمر رسمي بوجوب يجب تطبيق حماية الزاوية على مكبر صوت إذا قام المستخدم بتحديد شبكة أمامية معدنية.</span><span class="sxs-lookup"><span data-stu-id="95553-105">It shows how you can mandate that corner protection must be applied to a speaker if the user has selected a front grill in metal.</span></span> <span data-ttu-id="95553-106">يستخدم الإجراء المكون مكبر الصوت المتطور في شركة العرض التوضيحي USMF.</span><span class="sxs-lookup"><span data-stu-id="95553-106">The procedure uses the High end speaker component in the demo company USMF.</span></span>

## <a name="create-an-expression-constraint"></a><span data-ttu-id="95553-107">قم بإنشاء قيد تعبير</span><span class="sxs-lookup"><span data-stu-id="95553-107">Create an expression constraint</span></span>

1. <span data-ttu-id="95553-108">انتقل إلى **إدارة معلومات المنتج \> المنتجات \> نماذج تكوين المنتجات**.</span><span class="sxs-lookup"><span data-stu-id="95553-108">Go to **Product information management \> Products \> Product configuration models**.</span></span>
3. <span data-ttu-id="95553-109">في القائمة، قم بالبحث عن السجل المطلوب وحدده.</span><span class="sxs-lookup"><span data-stu-id="95553-109">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="95553-110">يستخدم هذا المثال نموذج مكبر الصوت المتطور.</span><span class="sxs-lookup"><span data-stu-id="95553-110">This example uses the high end speaker model.</span></span>  
4. <span data-ttu-id="95553-111">في القائمة، حدد الارتباط في الصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="95553-111">In the list, select the link in the selected row.</span></span>
5. <span data-ttu-id="95553-112">قم بتوسيع قسم **القيود**.</span><span class="sxs-lookup"><span data-stu-id="95553-112">Expand the **Constraints** section.</span></span>
6. <span data-ttu-id="95553-113">حدد **إضافة**.</span><span class="sxs-lookup"><span data-stu-id="95553-113">Select **Add**.</span></span>
7. <span data-ttu-id="95553-114">حدد **إنشاء**.</span><span class="sxs-lookup"><span data-stu-id="95553-114">Select **Create**.</span></span>
8. <span data-ttu-id="95553-115">في الحقل **الاسم**، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="95553-115">In the **Name** field, type a value.</span></span>

## <a name="enter-expression"></a><span data-ttu-id="95553-116">إدخال تعبير</span><span class="sxs-lookup"><span data-stu-id="95553-116">Enter expression</span></span>

1. <span data-ttu-id="95553-117">حدد **تحرير التعبير**.</span><span class="sxs-lookup"><span data-stu-id="95553-117">Select **Edit expression**.</span></span>
    * <span data-ttu-id="95553-118">إذا قمت بإلغاء تأمين واجهة المستخدم في تسجيل المهمة في هذه المرحلة، يمكنك استخدام IntelliSense وقائمة من الرموز لإنشاء تعبير القيد.</span><span class="sxs-lookup"><span data-stu-id="95553-118">If you unlock the user interface in the task recording at this stage, you can use IntelliSense and the list of symbols to build the constraint expression .</span></span>  
2. <span data-ttu-id="95553-119">في حقل **ConstraintBody**، أدخل 'Implies[FrontGrill=="Metal", CornerProtection] '.</span><span class="sxs-lookup"><span data-stu-id="95553-119">In the **ConstraintBody** field, enter 'Implies[FrontGrill=="Metal", CornerProtection] '.</span></span>
    * <span data-ttu-id="95553-120">يوضح منطق التعبير هذا: إذا كانت الشبكة الأمامية معدنية، فيجب تحديد خيار حماية الزاوية.</span><span class="sxs-lookup"><span data-stu-id="95553-120">This expression logic states: If the Front grill is  metal, then the corner protection option must be selected.</span></span>  
3. <span data-ttu-id="95553-121">حدد **التحقق من الصحة**.</span><span class="sxs-lookup"><span data-stu-id="95553-121">Select **Validate**.</span></span>
    * <span data-ttu-id="95553-122">يتم تشغيل دالة التحقق من الصحة من خلال تعبير القيد وتتحقق من وجود أخطاء في بناء الجملة.</span><span class="sxs-lookup"><span data-stu-id="95553-122">The validate function runs through the constraint expression and checks for syntax errors.</span></span>  
4. <span data-ttu-id="95553-123">حدد **إغلاق**.</span><span class="sxs-lookup"><span data-stu-id="95553-123">Select **Close**.</span></span>
5. <span data-ttu-id="95553-124">حدد **موافق**.</span><span class="sxs-lookup"><span data-stu-id="95553-124">Select **OK**.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]