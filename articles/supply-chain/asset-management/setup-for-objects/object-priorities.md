---
title: مستويات خدمة الأصول
description: يشرح هذا الموضوع مستويات الأصول في إدارة الأصول.
author: josaw1
manager: AnnBe
ms.date: 06/26/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CatProcureCatalogEdit, CatProcureCatalogListPage
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 2214
ms.assetid: 2f3e0441-414d-402b-b28b-7ab0d650d658
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 6dad0cb480f69eac84df5ea9a67f2adb94e2f52c
ms.sourcegitcommit: 57bc7e17682e2edb5e1766496b7a22f4621819dd
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 11/18/2019
ms.locfileid: "2811793"
---
# <a name="asset-service-levels"></a><span data-ttu-id="55aaf-103">مستويات خدمة الأصول</span><span class="sxs-lookup"><span data-stu-id="55aaf-103">Asset service levels</span></span>

[!include [banner](../../includes/banner.md)]

 

<span data-ttu-id="55aaf-104">يشرح هذا الموضوع مستويات الأصول في إدارة الأصول.</span><span class="sxs-lookup"><span data-stu-id="55aaf-104">This topic explains asset service levels in Asset Management.</span></span> <span data-ttu-id="55aaf-105">ترتبط مستويات خدمة الأصول بالأصول، ويتم نقلها إلى طلبات الصيانة وأوامر العمل.</span><span class="sxs-lookup"><span data-stu-id="55aaf-105">Asset service levels are related to assets, and are transferred to maintenance requests and work orders.</span></span> <span data-ttu-id="55aaf-106">وتُستخدم لحساب أولوية أوامر العمل أثناء جدولة أوامر العمل.</span><span class="sxs-lookup"><span data-stu-id="55aaf-106">They are used to calculate the priority of work orders during work order scheduling.</span></span> <span data-ttu-id="55aaf-107">يمكن تغيير مستويات خدمة الأصول، إذا كانت التغييرات مطلوبة.</span><span class="sxs-lookup"><span data-stu-id="55aaf-107">Asset service levels can be changed, if changes are required.</span></span>

<span data-ttu-id="55aaf-108">لمزيد من المعلومات حول الإعداد المرتبط بحساب درجات التقييم لجدولة أمر العمل، راجع [معلمات إدارة الأصول](../setup-for-objects/enterprise-asset-management-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="55aaf-108">For more information about the setup that is related to the calculation of rating scores for work order scheduling, see [Asset Management parameters](../setup-for-objects/enterprise-asset-management-parameters.md).</span></span> <span data-ttu-id="55aaf-109">يجب إعداد سجل افتراضي واحد على الأقل لمستوى خدمة الأصول.</span><span class="sxs-lookup"><span data-stu-id="55aaf-109">You must set up at least one default record for the asset service level.</span></span> <span data-ttu-id="55aaf-110">يتم استخدام هذا السجل الافتراضي في حالة عدم العثور على تطابق آخر أثناء جدولة أمر العمل.</span><span class="sxs-lookup"><span data-stu-id="55aaf-110">This default record is used if no other match is found during work order scheduling.</span></span>

<span data-ttu-id="55aaf-111">**مثال 1:** مستوى الخدمة الافتراضي المستخدم في حالة عدم العثور على تطابق آخر.</span><span class="sxs-lookup"><span data-stu-id="55aaf-111">**Example 1:** The default service level that is used if no other match is found.</span></span> <span data-ttu-id="55aaf-112">في هذا السجل، تحدد مستوى خدمة واحدًا فقط.</span><span class="sxs-lookup"><span data-stu-id="55aaf-112">In this record, you select only a service level.</span></span>

<span data-ttu-id="55aaf-113">**مثال 2:** مستوى خدمة عالٍ يُستخدم لجدولة مهام محرك شاحنة Volvo.</span><span class="sxs-lookup"><span data-stu-id="55aaf-113">**Example 2:** A high service level that is used to schedule jobs for a Volvo truck engine.</span></span> <span data-ttu-id="55aaf-114">في هذا السجل، تحدد نوع أصل ذا صلة (مثل **محرك شاحنة**) وشركة مصنعة (**Volvo**) ومستوى خدمة.</span><span class="sxs-lookup"><span data-stu-id="55aaf-114">In this record, you select a relevant asset type (such as **Truck Engine**), a manufacturer (**Volvo**), and a service level.</span></span>

## <a name="set-up-asset-service-levels"></a><span data-ttu-id="55aaf-115">إعداد مستويات خدمة الأصول</span><span class="sxs-lookup"><span data-stu-id="55aaf-115">Set up asset service levels</span></span>

1. <span data-ttu-id="55aaf-116">حدد **إدارة الأصول** \> **إعداد** \> **مستويات خدمة الأصول**.</span><span class="sxs-lookup"><span data-stu-id="55aaf-116">Select **Asset management** \> **Setup** \> **Asset service levels**.</span></span>
2. <span data-ttu-id="55aaf-117">حدد **جديد** لإنشاء سجل.</span><span class="sxs-lookup"><span data-stu-id="55aaf-117">Select **New** to create a record.</span></span>
3. <span data-ttu-id="55aaf-118">وفقًا لمستوى التفاصيل المطلوب لمستوى خدمة الأصول، قم بإجراء تحديدات ذات صلة في الحقول التالية **موقع العمل** و**نوع الأصل** و**الشركة المصنعة** و**النموذج** و**الأصل‏‎** و**نوع أمر العمل** و**مستوى الخدمة**.</span><span class="sxs-lookup"><span data-stu-id="55aaf-118">Depending on the detail level that is required for the asset service level, make relevant selections in the **Functional location**, **Asset type**, **Manufacturer**, **Model**, **Asset**, **Work order type**, and **Service level** fields.</span></span>

    > [!NOTE]
    > <span data-ttu-id="55aaf-119">عند استخدام مستوى خدمة الأصول لطلبات الصيانة وأوامر العمل، تجري إدارة الأصول مراجع لجميع سجلات مستوى خدمة الأصول للتحقق من وجود تطابق محتمل.</span><span class="sxs-lookup"><span data-stu-id="55aaf-119">When the asset service level is used for maintenance requests and work orders, Asset Management goes through all asset service level records to check for a possible match.</span></span> <span data-ttu-id="55aaf-120">وهي تتحقق دائمًا من المجموعة الأكثر تحديدًا أولاً.</span><span class="sxs-lookup"><span data-stu-id="55aaf-120">It always checks the most specific combination first.</span></span> <span data-ttu-id="55aaf-121">وبعبارة أخرى، تقوم إدارة الأصول أولاً بالتحقق من تطابق في حقل **نوع أمر العمل**.</span><span class="sxs-lookup"><span data-stu-id="55aaf-121">In other words, Asset Management first checks for a match for the **Work order type** field.</span></span> <span data-ttu-id="55aaf-122">إذا لم يتم العثور على تطابق، فهي تتحقق من وجود تطابق لحقل **الأصل**.</span><span class="sxs-lookup"><span data-stu-id="55aaf-122">If no match is found, it checks for a match for the **Asset** field, and so on.</span></span> <span data-ttu-id="55aaf-123">كما ترى في تخطيط الصفحة **مستويات خدمة الأصول**، يعني هذا السلوك أنه، للعثور على المجموعة الأكثر تحديدًا، تقوم إدارة الأصول بالتحقق من كل سجل من اليسار إلى اليمين للحصول على تطابق.</span><span class="sxs-lookup"><span data-stu-id="55aaf-123">As you can see in the layout of the **Asset service levels** page, this behavior means that, to find the most specific combination, Asset Management checks each record from right to left for a match.</span></span> <span data-ttu-id="55aaf-124">إذا لم يتم العثور على تطابق، يتم استخدام السجل الافتراضي الذي لا يحتوي على تحديدات في هذه الحقول.</span><span class="sxs-lookup"><span data-stu-id="55aaf-124">If no match is found, the default record that has no selections in those fields is used.</span></span>

4. <span data-ttu-id="55aaf-125">في الحقل‏‎ **مستوى الخدمة**، حدد رقمًا يشير إلى مستوى الخدمة (أولوية).</span><span class="sxs-lookup"><span data-stu-id="55aaf-125">In the **Service level** field, select a number that indicates the service level (priority).</span></span>


> [!NOTE]
> <span data-ttu-id="55aaf-126">إذا قمت بتغيير سجل مستوى الخدمة في صفحة **مستويات خدمة الأصول** بعد استخدامه في أمر عمل، فلن يتم تحديث مستوى الخدمة في طلبات الصيانة وأوامر العمل وفقًا لذلك.</span><span class="sxs-lookup"><span data-stu-id="55aaf-126">If you change an asset service level record on the **Asset service levels** page after you've already used it on a work order, the service level on maintenance requests and work orders isn't updated accordingly.</span></span>
