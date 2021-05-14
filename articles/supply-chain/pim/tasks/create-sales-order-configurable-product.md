---
title: إنشاء أمر مبيعات لمنتج قابل للتكوين
description: يوضح هذا الإجراء كيفية تطبيق قالب تكوين على منتج في أمر مبيعات.
author: ShylaThompson
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: DefaultDashboard, SalesOrderProcessingWorkspace, SalesCreateOrder, SalesTable, PCRuntimeConfigurator, PCTemplateConfigurationSelection
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 8607de5705354aa58c985fb536f3e1d52acd1f37
ms.sourcegitcommit: fa99a36c3d30d0c0577fd3f63ed6bf2f71599e40
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 04/20/2021
ms.locfileid: "5921279"
---
# <a name="create-a-sales-order-for-a-configurable-product"></a><span data-ttu-id="ad4ac-103">إنشاء أمر مبيعات لمنتج قابل للتكوين</span><span class="sxs-lookup"><span data-stu-id="ad4ac-103">Create a sales order for a configurable product</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="ad4ac-104">يوضح هذا الإجراء كيفية تطبيق قالب تكوين على منتج في أمر مبيعات.</span><span class="sxs-lookup"><span data-stu-id="ad4ac-104">This procedure shows how to apply a configuration template to a product on a sales order.</span></span> <span data-ttu-id="ad4ac-105">يستخدم هذا المثال نموذج مكبر الصوت المتطور D0006 في شركة بيانات العرض التوضيحي USMF.</span><span class="sxs-lookup"><span data-stu-id="ad4ac-105">This example uses the D0006 speaker model in the USMF demo data company.</span></span> <span data-ttu-id="ad4ac-106">يستخدم معالج أمر المبيعات عادةً هذا الإجراء.</span><span class="sxs-lookup"><span data-stu-id="ad4ac-106">Typically, a sales order processor uses this procedure.</span></span>

## <a name="create-a-sales-order"></a><span data-ttu-id="ad4ac-107">إنشاء أمر مبيعات</span><span class="sxs-lookup"><span data-stu-id="ad4ac-107">Create a sales order</span></span>

1. <span data-ttu-id="ad4ac-108">انتقل إلى **المبيعات والتسويق \> مساحات العمل \> معالجة أوامر المبيعات والاستعلام عنها**.</span><span class="sxs-lookup"><span data-stu-id="ad4ac-108">Go to **Sales and marketing \> Workspaces \> Sales order processing and inquiry**.</span></span>
1. <span data-ttu-id="ad4ac-109">حدد **جديد**.</span><span class="sxs-lookup"><span data-stu-id="ad4ac-109">Select **New**.</span></span>
1. <span data-ttu-id="ad4ac-110">حدد **أمر المبيعات**.</span><span class="sxs-lookup"><span data-stu-id="ad4ac-110">Select **Sales order**.</span></span>
1. <span data-ttu-id="ad4ac-111">في حقل **حساب العميل**، حدد *US-001*.</span><span class="sxs-lookup"><span data-stu-id="ad4ac-111">In the **Customer account** field, select *US-001*.</span></span> 
1. <span data-ttu-id="ad4ac-112">حدد **موافق**.</span><span class="sxs-lookup"><span data-stu-id="ad4ac-112">Select **OK**.</span></span>
1. <span data-ttu-id="ad4ac-113">في حقل **رقم الصنف**، حدد *D0006*.</span><span class="sxs-lookup"><span data-stu-id="ad4ac-113">In the **Item number** field, select *D0006*.</span></span>
    * <span data-ttu-id="ad4ac-114">لتنفيذ هذه المهمة، يجب تحديد منتج قابل للتكوين.</span><span class="sxs-lookup"><span data-stu-id="ad4ac-114">For this task, you must select a configurable product.</span></span>  
1. <span data-ttu-id="ad4ac-115">حدد **المنتج والتوريد**.</span><span class="sxs-lookup"><span data-stu-id="ad4ac-115">Select **Product and supply**.</span></span>
1. <span data-ttu-id="ad4ac-116">حدد **تكوين البند**.</span><span class="sxs-lookup"><span data-stu-id="ad4ac-116">Select **Configure line**.</span></span>
    * <span data-ttu-id="ad4ac-117">لاحظ أن السعر قد تغيّر، استنادًا إلى التكوين الذي تم تحديده، وأن الحقل **تضمين الكبل** أصبح الآن معينًا إلى *True*.</span><span class="sxs-lookup"><span data-stu-id="ad4ac-117">Note that the price has changed, based on the configuration that was selected, and that the **Include cable** field is now set to *True*.</span></span>  
    * <span data-ttu-id="ad4ac-118">لاحظ أنه تم تحديد السعر الافتراضي والإعدادات للكبل.</span><span class="sxs-lookup"><span data-stu-id="ad4ac-118">Note the default price and the settings that are selected for the cable.</span></span>  
1. <span data-ttu-id="ad4ac-119">حدد **تحميل قالب**.</span><span class="sxs-lookup"><span data-stu-id="ad4ac-119">Select **Load template**.</span></span>
    * <span data-ttu-id="ad4ac-120">يوضح هذا المثال كيفية تطبيق قالب لتحديد تكوين معرّف مسبقًا.</span><span class="sxs-lookup"><span data-stu-id="ad4ac-120">This example shows how you can apply a template to select a predefined configuration.</span></span> <span data-ttu-id="ad4ac-121">إذا كنت تستخدم هذا الإجراء كدليل مهمة وأردت رؤية قيم السمات الأخرى المتوفرة، فيجب تحديد الزر **إلغاء قفل**.</span><span class="sxs-lookup"><span data-stu-id="ad4ac-121">If you're using this procedure as a task guide and want to see the other attribute values that are available, you must select the **Unlock** button.</span></span>  
1. <span data-ttu-id="ad4ac-122">حدد **موافق**.</span><span class="sxs-lookup"><span data-stu-id="ad4ac-122">Select **OK**.</span></span>
1. <span data-ttu-id="ad4ac-123">حدد **موافق**.</span><span class="sxs-lookup"><span data-stu-id="ad4ac-123">Select **OK**.</span></span>
1. <span data-ttu-id="ad4ac-124">قم بتوسيع قسم **تفاصيل البند**.</span><span class="sxs-lookup"><span data-stu-id="ad4ac-124">Expand the **Line details** section.</span></span>
1. <span data-ttu-id="ad4ac-125">حدد علامة التبويب **منتج**.</span><span class="sxs-lookup"><span data-stu-id="ad4ac-125">Select the **Product** tab.</span></span>
    * <span data-ttu-id="ad4ac-126">تم الآن إدراج تكوين الصنف ضمن أبعاد المنتج.</span><span class="sxs-lookup"><span data-stu-id="ad4ac-126">The configuration of the item is now listed under the product dimensions.</span></span>  
1. <span data-ttu-id="ad4ac-127">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="ad4ac-127">Close the page.</span></span>


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]