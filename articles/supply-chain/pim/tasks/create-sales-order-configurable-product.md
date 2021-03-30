---
title: إنشاء أمر مبيعات لمنتج قابل للتكوين
description: يوضح هذا الإجراء كيفية تطبيق قالب تكوين على منتج في أمر مبيعات.
author: ShylaThompson
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: DefaultDashboard, SalesOrderProcessingWorkspace, SalesCreateOrder, SalesTable, PCRuntimeConfigurator, PCTemplateConfigurationSelection
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: d9a9b60fbcf6de5377b44ca03d4ffc792a6a78f4
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 02/15/2021
ms.locfileid: "5206981"
---
# <a name="create-a-sales-order-for-a-configurable-product"></a><span data-ttu-id="30a3e-103">إنشاء أمر مبيعات لمنتج قابل للتكوين</span><span class="sxs-lookup"><span data-stu-id="30a3e-103">Create a sales order for a configurable product</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="30a3e-104">يوضح هذا الإجراء كيفية تطبيق قالب تكوين على منتج في أمر مبيعات.</span><span class="sxs-lookup"><span data-stu-id="30a3e-104">This procedure shows how to apply a configuration template to a product on a sales order.</span></span> <span data-ttu-id="30a3e-105">يستخدم هذا المثال نموذج مكبر الصوت المتطور D0006 في شركة بيانات العرض التوضيحي USMF.</span><span class="sxs-lookup"><span data-stu-id="30a3e-105">This example uses the D0006 speaker model in the USMF demo data company.</span></span> <span data-ttu-id="30a3e-106">يستخدم معالج أمر المبيعات عادةً هذا الإجراء.</span><span class="sxs-lookup"><span data-stu-id="30a3e-106">Typically, a sales order processor uses this procedure.</span></span>


## <a name="create-a-sales-order"></a><span data-ttu-id="30a3e-107">إنشاء أمر مبيعات</span><span class="sxs-lookup"><span data-stu-id="30a3e-107">Create a sales order</span></span>
1. <span data-ttu-id="30a3e-108">انقر فوق "الاستعلام عن أمر المبيعات ومعالجته‬".</span><span class="sxs-lookup"><span data-stu-id="30a3e-108">Click Sales order processing and inquiry.</span></span>
2. <span data-ttu-id="30a3e-109">انقر فوق "جديد".</span><span class="sxs-lookup"><span data-stu-id="30a3e-109">Click New.</span></span>
3. <span data-ttu-id="30a3e-110">انقر فوق "أمر المبيعات".</span><span class="sxs-lookup"><span data-stu-id="30a3e-110">Click Sales order.</span></span>
4. <span data-ttu-id="30a3e-111">في حقل "حساب العميل"، حدد US-001.</span><span class="sxs-lookup"><span data-stu-id="30a3e-111">In the Customer account field, select US-001.</span></span> 
5. <span data-ttu-id="30a3e-112">انقر فوق "موافق".</span><span class="sxs-lookup"><span data-stu-id="30a3e-112">Click OK.</span></span>
6. <span data-ttu-id="30a3e-113">في حقل "رقم الصنف"، حدد D0006.</span><span class="sxs-lookup"><span data-stu-id="30a3e-113">In the Item number field, select D0006.</span></span>
    * <span data-ttu-id="30a3e-114">لتنفيذ هذه المهمة، يجب تحديد منتج قابل للتكوين.</span><span class="sxs-lookup"><span data-stu-id="30a3e-114">For this task, you must select a configurable product.</span></span>  
7. <span data-ttu-id="30a3e-115">انقر فوق "المنتج والتوريد".</span><span class="sxs-lookup"><span data-stu-id="30a3e-115">Click Product and supply.</span></span>
8. <span data-ttu-id="30a3e-116">انقر فوق تكوين البند.</span><span class="sxs-lookup"><span data-stu-id="30a3e-116">Click Configure line.</span></span>
    * <span data-ttu-id="30a3e-117">لاحظ أن السعر قد تغيّر، استنادًا إلى التكوين الذي تم تحديده، وأن الحقل "تضمين الكبل" أصبح الآن معينًا إلى True.</span><span class="sxs-lookup"><span data-stu-id="30a3e-117">Note that the price has changed, based on the configuration that was selected, and that the Include cable field is now set to True.</span></span>  
    * <span data-ttu-id="30a3e-118">لاحظ أنه تم تحديد السعر الافتراضي والإعدادات للكبل.</span><span class="sxs-lookup"><span data-stu-id="30a3e-118">Note the default price and the settings that are selected for the cable.</span></span>  
9. <span data-ttu-id="30a3e-119">انقر فوق تحميل القالب.</span><span class="sxs-lookup"><span data-stu-id="30a3e-119">Click Load template.</span></span>
    * <span data-ttu-id="30a3e-120">يوضح هذا المثال كيفية تطبيق قالب لتحديد تكوين معرّف مسبقًا.</span><span class="sxs-lookup"><span data-stu-id="30a3e-120">This example shows how you can apply a template to select a predefined configuration.</span></span> <span data-ttu-id="30a3e-121">إذا كنت تستخدم هذا الإجراء كدليل مهمة وأردت رؤية قيم السمات الأخرى المتوفرة، فيجب النقر فوق الزر "إلغاء التأمين".</span><span class="sxs-lookup"><span data-stu-id="30a3e-121">If you're using this procedure as a task guide and want to see the other attribute values that are available, you must click the Unlock button.</span></span>  
10. <span data-ttu-id="30a3e-122">انقر فوق "موافق".</span><span class="sxs-lookup"><span data-stu-id="30a3e-122">Click OK.</span></span>
11. <span data-ttu-id="30a3e-123">انقر فوق "موافق".</span><span class="sxs-lookup"><span data-stu-id="30a3e-123">Click OK.</span></span>
12. <span data-ttu-id="30a3e-124">قم بتوسيع قسم "تفاصيل البند".</span><span class="sxs-lookup"><span data-stu-id="30a3e-124">Expand the Line details section.</span></span>
13. <span data-ttu-id="30a3e-125">انقر فوق علامة التبويب "المنتج".</span><span class="sxs-lookup"><span data-stu-id="30a3e-125">Click the Product tab.</span></span>
    * <span data-ttu-id="30a3e-126">تم الآن إدراج تكوين الصنف ضمن أبعاد المنتج.</span><span class="sxs-lookup"><span data-stu-id="30a3e-126">The configuration of the item is now listed under the product dimensions.</span></span>  
14. <span data-ttu-id="30a3e-127">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="30a3e-127">Close the page.</span></span>

## <a name="select-the-product-configuration"></a><span data-ttu-id="30a3e-128">تحديد تكوين المنتج</span><span class="sxs-lookup"><span data-stu-id="30a3e-128">Select the product configuration</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]