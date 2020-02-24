---
title: المتطلبات الأساسية‬ لإعداد قناة
description: يقدم هذا الموضوع نظرة عامة على المتطلبات الأساسية لإعداد القناة في Microsoft Dynamics 365 Commerce.
author: samjarawan
manager: annbe
ms.date: 01/27/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: samjar
ms.search.validFrom: 2020-01-20
ms.dyn365.ops.version: Release 10.0.8
ms.openlocfilehash: b861d90f1333c8f6e61a83602ed74e30b65f3dc1
ms.sourcegitcommit: 81a647904dd305c4be2e4b683689f128548a872d
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 02/01/2020
ms.locfileid: "3002279"
---
# <a name="channel-setup-prerequisites"></a><span data-ttu-id="e6fbd-103">المتطلبات الأساسية‬ لإعداد قناة</span><span class="sxs-lookup"><span data-stu-id="e6fbd-103">Channel setup prerequisites</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="e6fbd-104">يقدم هذا الموضوع نظرة عامة على المتطلبات الأساسية لإعداد القناة في Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="e6fbd-104">This topic presents an overview of channel setup prerequisites in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="e6fbd-105">نظرة عامة</span><span class="sxs-lookup"><span data-stu-id="e6fbd-105">Overview</span></span>

<span data-ttu-id="e6fbd-106">قبل أن تتمكن من إنشاء قناة Dynamics 365 Commerce، يجب إكمال العديد من المهام الأساسية.</span><span class="sxs-lookup"><span data-stu-id="e6fbd-106">Before a Dynamics 365 Commerce channel can be created, several prerequisite tasks must be completed.</span></span> <span data-ttu-id="e6fbd-107">يتم تنظيم القوائم التالية للمهام الأساسية حسب نوع القناة.</span><span class="sxs-lookup"><span data-stu-id="e6fbd-107">The following lists of prerequisite tasks are organized by channel type.</span></span>

> [!NOTE]
> <span data-ttu-id="e6fbd-108">لا تزال بعض الوثائق قيد الكتابة، وسيتم تحديث الارتباطات عند نشر محتوى جديد.</span><span class="sxs-lookup"><span data-stu-id="e6fbd-108">Some documentation is still being written, and links will be updated as new content is published.</span></span>

## <a name="initialization"></a><span data-ttu-id="e6fbd-109">بدء</span><span class="sxs-lookup"><span data-stu-id="e6fbd-109">Initialization</span></span>

- [<span data-ttu-id="e6fbd-110">تهيئة البيانات الأولية</span><span class="sxs-lookup"><span data-stu-id="e6fbd-110">Initialize seed data</span></span>](../retail/enable-configure-retail-functionality.md)

## <a name="global-prerequisities-required-for-all-channel-types"></a><span data-ttu-id="e6fbd-111">المتطلبات الأساسية العمومية لكل أنواع القنوات</span><span class="sxs-lookup"><span data-stu-id="e6fbd-111">Global prerequisities required for all channel types</span></span>

- [<span data-ttu-id="e6fbd-112">تعريف بنية الكيان القانوني وتكوينها</span><span class="sxs-lookup"><span data-stu-id="e6fbd-112">Define and configure your legal entity structure</span></span>](channels-legal-entities.md) 
- [<span data-ttu-id="e6fbd-113">تكوين التدرج الهرمي للمؤسسات</span><span class="sxs-lookup"><span data-stu-id="e6fbd-113">Configure your organizational hierarchy</span></span>](channels-org-hierarchies.md)
- [<span data-ttu-id="e6fbd-114">إعداد مستودع</span><span class="sxs-lookup"><span data-stu-id="e6fbd-114">Set up a warehouse</span></span>](channels-setup-warehouse.md)
- [<span data-ttu-id="e6fbd-115">تكوين ضريبة المبيعات</span><span class="sxs-lookup"><span data-stu-id="e6fbd-115">Configure sales tax</span></span>](https://docs.microsoft.com/en-us/dynamics365/finance/general-ledger/indirect-taxes-overview?toc=/dynamics365/commerce/toc.json)
- [<span data-ttu-id="e6fbd-116">إعداد ملف تعريف إخطار البريد الإلكتروني</span><span class="sxs-lookup"><span data-stu-id="e6fbd-116">Set up an email notification profile</span></span>](email-notification-profiles.md)
- [<span data-ttu-id="e6fbd-117">إعداد التسلسلات الرقمية</span><span class="sxs-lookup"><span data-stu-id="e6fbd-117">Set up number sequences</span></span>](https://docs.microsoft.com/en-us/dynamics365/fin-ops-core/fin-ops/organization-administration/number-sequence-overview?toc=/dynamics365/commerce/toc.json)
- [<span data-ttu-id="e6fbd-118">إعداد عميل ودفتر عناوين افتراضيين</span><span class="sxs-lookup"><span data-stu-id="e6fbd-118">Set up a default customer and address book</span></span>](default-customer.md)
<!--
- [Configure commerce parameters](commerce-parameters.md)
-->

## <a name="retail-channel-prerequisites"></a><span data-ttu-id="e6fbd-119">المتطلبات الأساسية‬ لقناة البيع بالتجزئة</span><span class="sxs-lookup"><span data-stu-id="e6fbd-119">Retail channel prerequisites</span></span>

- [<span data-ttu-id="e6fbd-120">أكواد المعلومات ومجموعات أكواد المعلومات</span><span class="sxs-lookup"><span data-stu-id="e6fbd-120">Info codes and info code groups</span></span>](https://docs.microsoft.com/en-us/dynamics365/retail/info-codes-retail?toc=/dynamics365/commerce/toc.json)
- [<span data-ttu-id="e6fbd-121">إعداد ملف تعريف وظائف البيع بالتجزئة</span><span class="sxs-lookup"><span data-stu-id="e6fbd-121">Set up a retail functionality profile</span></span>](retail-functionality-profile.md)
- [<span data-ttu-id="e6fbd-122">إعداد دفتر عناوين للموظفين</span><span class="sxs-lookup"><span data-stu-id="e6fbd-122">Set up an employee address book</span></span>](new-address-book.md)
- [<span data-ttu-id="e6fbd-123">إعداد تخطيط الشاشة</span><span class="sxs-lookup"><span data-stu-id="e6fbd-123">Set up a screen layout</span></span>](https://docs.microsoft.com/en-us/dynamics365/retail/pos-screen-layouts?toc=/dynamics365/commerce/toc.json)
- [<span data-ttu-id="e6fbd-124">إعداد محطة أجهزة</span><span class="sxs-lookup"><span data-stu-id="e6fbd-124">Set up a hardware station</span></span>](https://docs.microsoft.com/en-us/dynamics365/retail/retail-hardware-station-configuration-installation?toc=/dynamics365/commerce/toc.json)

## <a name="call-center-channel-prerequisites"></a><span data-ttu-id="e6fbd-125">المتطلبات الأساسية لقناة مركز الاتصال</span><span class="sxs-lookup"><span data-stu-id="e6fbd-125">Call Center channel prerequisites</span></span>

- <span data-ttu-id="e6fbd-126">محددات مركز الاتصال</span><span class="sxs-lookup"><span data-stu-id="e6fbd-126">Call center parameters</span></span>
- <span data-ttu-id="e6fbd-127">طرق استرداد مبالغ مراكز الاتصال</span><span class="sxs-lookup"><span data-stu-id="e6fbd-127">Call center refund methods</span></span>
- <span data-ttu-id="e6fbd-128">أنواع الإيجار</span><span class="sxs-lookup"><span data-stu-id="e6fbd-128">Rental types</span></span>
- <span data-ttu-id="e6fbd-129">خدمات الدفع</span><span class="sxs-lookup"><span data-stu-id="e6fbd-129">Payment services</span></span>
- <span data-ttu-id="e6fbd-130">أكواد تعليق الأمر</span><span class="sxs-lookup"><span data-stu-id="e6fbd-130">Order hold codes</span></span>

## <a name="online-channel-prerequisites"></a><span data-ttu-id="e6fbd-131">المتطلبات الأساسية‬ لقناة عبر الإنترنت</span><span class="sxs-lookup"><span data-stu-id="e6fbd-131">Online channel prerequisites</span></span>

- [<span data-ttu-id="e6fbd-132">إنشاء ملف تعريف الوظائف عبر الإنترنت</span><span class="sxs-lookup"><span data-stu-id="e6fbd-132">Create an online functionality profile</span></span>](online-functionality-profile.md)

## <a name="additional-resources"></a><span data-ttu-id="e6fbd-133">الموارد الإضافية</span><span class="sxs-lookup"><span data-stu-id="e6fbd-133">Additional resources</span></span>

[<span data-ttu-id="e6fbd-134">نظرة عامة على القنوات</span><span class="sxs-lookup"><span data-stu-id="e6fbd-134">Channels overview</span></span>](channels-overview.md)

[<span data-ttu-id="e6fbd-135">نظرة عامة المؤسسات والتدرجات الهرمية للمؤسسات</span><span class="sxs-lookup"><span data-stu-id="e6fbd-135">Organizations and organizational hierarchies overview</span></span>](../fin-ops-core/fin-ops/organization-administration/organizations-organizational-hierarchies.md?toc=/dynamics365/commerce/toc.json)

[<span data-ttu-id="e6fbd-136">إعداد التدرجات الهرمية للمؤسسات</span><span class="sxs-lookup"><span data-stu-id="e6fbd-136">Set up organization hierarchies</span></span>](channels-org-hierarchies.md)

[<span data-ttu-id="e6fbd-137">إنشاء كيانات قانونية</span><span class="sxs-lookup"><span data-stu-id="e6fbd-137">Create legal entities</span></span>](channels-legal-entities.md)

[<span data-ttu-id="e6fbd-138">إعداد قناة بيع بالتجزئة</span><span class="sxs-lookup"><span data-stu-id="e6fbd-138">Set up a retail channel</span></span>](channel-setup-retail.md)
    
[<span data-ttu-id="e6fbd-139">إعداد قناة عبر الإنترنت</span><span class="sxs-lookup"><span data-stu-id="e6fbd-139">Set up an online channel</span></span>](channel-setup-online.md)
