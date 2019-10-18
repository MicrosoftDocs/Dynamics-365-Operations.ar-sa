---
title: ترتيب التنفيذ للمزامنة الأولية بين تطبيقات Finance and Operations وCommon Data Service
description: يحدد هذا الموضوع ترتيب المزامنة الذي يجب اتباعه لإنشاء البيانات الأولية.
author: RamaKrishnamoorthy
manager: AnnBe
ms.date: 07/25/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2019-07-15
ms.openlocfilehash: 3110cb809558d168e9d97f640701b249caf73f6c
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 09/27/2019
ms.locfileid: "2184498"
---
# <a name="execution-order-for-initial-synchronization-of-finance-and-operations-apps-and-common-data-service"></a><span data-ttu-id="cfe91-103">ترتيب التنفيذ للمزامنة الأولية بين تطبيقات Finance and Operations وCommon Data Service</span><span class="sxs-lookup"><span data-stu-id="cfe91-103">Execution order for initial synchronization of Finance and Operations apps and Common Data Service</span></span>

[!include [banner](../includes/banner.md)]

[!include [preview](../includes/preview-banner.md)]

<span data-ttu-id="cfe91-104">قبل استخدام تكامل البيانات، يجب إنشاء البيانات الأولية المطلوبة للعملاء والموردين وجهات الاتصال.</span><span class="sxs-lookup"><span data-stu-id="cfe91-104">Before you use data integration, you must create the initial data that is required for customers, vendors, and contacts.</span></span> <span data-ttu-id="cfe91-105">على سبيل المثال، تريد إنشاء صنف **مجموعة مورّدين** وتعيين قيمة **شروط الدفع** لها إلى **Net30**.</span><span class="sxs-lookup"><span data-stu-id="cfe91-105">For example, you want to create a new **Vendor group** item and set its **Terms of Payment** value to **Net30**.</span></span> <span data-ttu-id="cfe91-106">في هذه الحالة، قبل أن تحاول إنشاء صنف **مجموعة المورّدين**، يجب أن تتأكد من وجود **Net30** في كل من التطبيق وCommon Data Service.</span><span class="sxs-lookup"><span data-stu-id="cfe91-106">In this case, before you try to create the **Vendor group** item, you must make sure that **Net30** exists in both the application and Common Data Service.</span></span> <span data-ttu-id="cfe91-107">(في المستقبل، ستقوم Microsoft بإصدار وظيفة نظام أساسي للكتابة المزدوجة تسمى المزامنة الأولية. ستجري هذه الوظيفة مزامنة بيانات لمرة واحدة بين التطبيق وCommon Data Service كجزء من إعداد الكتابة المزدوجة.)</span><span class="sxs-lookup"><span data-stu-id="cfe91-107">(In the future, Microsoft will release dual-write platform functionality that is named Initial Sync. This functionality will do a one-time data synchronization between the application and Common Data Service as part of the dual-write setup.)</span></span>

> [!TIP]
> <span data-ttu-id="cfe91-108">تعمل Microsoft على إصار خريطة كتابة مزدوجة لجميع البيانات المرجعية بما في ذلك **شروط الدفع** (شروط الدفع).</span><span class="sxs-lookup"><span data-stu-id="cfe91-108">Microsoft is releasing a dual-write map for all reference data, including **Terms of Payment** (payment terms).</span></span> <span data-ttu-id="cfe91-109">إذا كانت البيانات الأولية موجودة في نظام واحد، فبإمكان عملية تحديث صغيرة على سجل أن تؤدي تشغيل الكتابة المزدوجة على هذا السجل.</span><span class="sxs-lookup"><span data-stu-id="cfe91-109">If you already have the initial data in one system, a small update operation on a record can trigger dual-write on that record.</span></span>

<span data-ttu-id="cfe91-110">يجب اتباع ترتيب الأسبقية التالي والتأكد من توفر البيانات الأولية في التطبيق وCommon Data Service.</span><span class="sxs-lookup"><span data-stu-id="cfe91-110">You must follow the following order of precedence and make sure that the initial data is available in the application and Common Data Service.</span></span>

## <a name="vendor"></a><span data-ttu-id="cfe91-111">المورد</span><span class="sxs-lookup"><span data-stu-id="cfe91-111">Vendor</span></span>

<span data-ttu-id="cfe91-112">فيما يلي ترتيب التنفيذ الخاص بكيان **المورّد**:</span><span class="sxs-lookup"><span data-stu-id="cfe91-112">Here is the order of execution for the **Vendor** entity:</span></span>

1. <span data-ttu-id="cfe91-113">مجموعة الموردين</span><span class="sxs-lookup"><span data-stu-id="cfe91-113">Vendor group</span></span>

    1. <span data-ttu-id="cfe91-114">شروط الدفع</span><span class="sxs-lookup"><span data-stu-id="cfe91-114">Terms of payment</span></span>

        1. <span data-ttu-id="cfe91-115">يوم وبنود الدفع</span><span class="sxs-lookup"><span data-stu-id="cfe91-115">Payment day and lines</span></span>
        2. <span data-ttu-id="cfe91-116">جدول الدفع</span><span class="sxs-lookup"><span data-stu-id="cfe91-116">Payment schedule</span></span>

2. <span data-ttu-id="cfe91-117">طريقة دفع المورّد</span><span class="sxs-lookup"><span data-stu-id="cfe91-117">Vendor payment method</span></span>

## <a name="customer-organization"></a><span data-ttu-id="cfe91-118">العميل (مؤسسة)</span><span class="sxs-lookup"><span data-stu-id="cfe91-118">Customer (Organization)</span></span>

<span data-ttu-id="cfe91-119">فيما يلي ترتيب التنفيذ الخاص بكيان **العميل**:</span><span class="sxs-lookup"><span data-stu-id="cfe91-119">Here is the order of execution for the **Customer** entity:</span></span>

1. <span data-ttu-id="cfe91-120">مجموعة العملاء</span><span class="sxs-lookup"><span data-stu-id="cfe91-120">Customer group</span></span>

    1. <span data-ttu-id="cfe91-121">شروط الدفع</span><span class="sxs-lookup"><span data-stu-id="cfe91-121">Terms of payment</span></span>

        1. <span data-ttu-id="cfe91-122">يوم وبنود الدفع</span><span class="sxs-lookup"><span data-stu-id="cfe91-122">Payment day and lines</span></span>
        2. <span data-ttu-id="cfe91-123">المدفوعات</span><span class="sxs-lookup"><span data-stu-id="cfe91-123">Payment</span></span> 

2. <span data-ttu-id="cfe91-124">طريقة دفع العميل</span><span class="sxs-lookup"><span data-stu-id="cfe91-124">Customer payment method</span></span>

## <a name="contact-person"></a><span data-ttu-id="cfe91-125">جهة الاتصال (شخص)</span><span class="sxs-lookup"><span data-stu-id="cfe91-125">Contact (Person)</span></span>

<span data-ttu-id="cfe91-126">فيما يلي ترتيب التنفيذ الخاص بكيان **جهة الاتصال**:</span><span class="sxs-lookup"><span data-stu-id="cfe91-126">Here is the order of execution for the **Contact** entity:</span></span>

1. <span data-ttu-id="cfe91-127">العميل</span><span class="sxs-lookup"><span data-stu-id="cfe91-127">Customer</span></span>
2. <span data-ttu-id="cfe91-128">المورد</span><span class="sxs-lookup"><span data-stu-id="cfe91-128">Vendor</span></span>
