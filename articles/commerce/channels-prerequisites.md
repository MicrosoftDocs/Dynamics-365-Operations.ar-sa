---
title: المتطلبات الأساسية‬ لإعداد قناة
description: يقدم هذا الموضوع نظرة عامة على المتطلبات الأساسية لإعداد القناة في Microsoft Dynamics 365 Commerce.
author: samjarawan
manager: annbe
ms.date: 02/21/2020
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
ms.openlocfilehash: 0da0457240cf12686fff2fa929c7fb510c11f242
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 10/13/2020
ms.locfileid: "4409851"
---
# <a name="channel-setup-prerequisites"></a><span data-ttu-id="ccaec-103">المتطلبات الأساسية‬ لإعداد قناة</span><span class="sxs-lookup"><span data-stu-id="ccaec-103">Channel setup prerequisites</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="ccaec-104">يقدم هذا الموضوع نظرة عامة على المتطلبات الأساسية لإعداد القناة في Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="ccaec-104">This topic presents an overview of channel setup prerequisites in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="ccaec-105">نظرة عامة</span><span class="sxs-lookup"><span data-stu-id="ccaec-105">Overview</span></span>

<span data-ttu-id="ccaec-106">قبل أن تتمكن من إنشاء قناة Dynamics 365 Commerce، يجب إكمال العديد من المهام الأساسية.</span><span class="sxs-lookup"><span data-stu-id="ccaec-106">Before a Dynamics 365 Commerce channel can be created, several prerequisite tasks must be completed.</span></span> <span data-ttu-id="ccaec-107">يتم تنظيم القوائم التالية للمهام الأساسية حسب نوع القناة.</span><span class="sxs-lookup"><span data-stu-id="ccaec-107">The following lists of prerequisite tasks are organized by channel type.</span></span>

> [!NOTE]
> <span data-ttu-id="ccaec-108">لا تزال بعض الوثائق قيد الكتابة، وسيتم تحديث الارتباطات عند نشر محتوى جديد.</span><span class="sxs-lookup"><span data-stu-id="ccaec-108">Some documentation is still being written, and links will be updated as new content is published.</span></span>

## <a name="initialization"></a><span data-ttu-id="ccaec-109">بدء</span><span class="sxs-lookup"><span data-stu-id="ccaec-109">Initialization</span></span>

- [<span data-ttu-id="ccaec-110">تهيئة البيانات الأولية</span><span class="sxs-lookup"><span data-stu-id="ccaec-110">Initialize seed data</span></span>](enable-configure-retail-functionality.md)

## <a name="global-prerequisities-required-for-all-channel-types"></a><span data-ttu-id="ccaec-111">المتطلبات الأساسية العمومية لكل أنواع القنوات</span><span class="sxs-lookup"><span data-stu-id="ccaec-111">Global prerequisities required for all channel types</span></span>

- [<span data-ttu-id="ccaec-112">تعريف بنية الكيان القانوني وتكوينها</span><span class="sxs-lookup"><span data-stu-id="ccaec-112">Define and configure your legal entity structure</span></span>](channels-legal-entities.md) 
- [<span data-ttu-id="ccaec-113">تكوين التدرج الهرمي للمؤسسات</span><span class="sxs-lookup"><span data-stu-id="ccaec-113">Configure your organizational hierarchy</span></span>](channels-org-hierarchies.md)
- [<span data-ttu-id="ccaec-114">إعداد مستودع</span><span class="sxs-lookup"><span data-stu-id="ccaec-114">Set up a warehouse</span></span>](channels-setup-warehouse.md)
- [<span data-ttu-id="ccaec-115">تكوين ضريبة المبيعات</span><span class="sxs-lookup"><span data-stu-id="ccaec-115">Configure sales tax</span></span>](../finance/general-ledger/indirect-taxes-overview.md?toc=/dynamics365/commerce/toc.json)
- [<span data-ttu-id="ccaec-116">إعداد ملف تعريف إخطار البريد الإلكتروني</span><span class="sxs-lookup"><span data-stu-id="ccaec-116">Set up an email notification profile</span></span>](email-notification-profiles.md)
- [<span data-ttu-id="ccaec-117">إعداد التسلسلات الرقمية</span><span class="sxs-lookup"><span data-stu-id="ccaec-117">Set up number sequences</span></span>](../fin-ops-core/fin-ops/organization-administration/number-sequence-overview.md?toc=/dynamics365/commerce/toc.json)
- [<span data-ttu-id="ccaec-118">إعداد عميل ودفتر عناوين افتراضيين</span><span class="sxs-lookup"><span data-stu-id="ccaec-118">Set up a default customer and address book</span></span>](default-customer.md)
<!--
- [Configure commerce parameters](commerce-parameters.md)
-->

## <a name="retail-channel-prerequisites"></a><span data-ttu-id="ccaec-119">المتطلبات الأساسية‬ لقناة البيع بالتجزئة</span><span class="sxs-lookup"><span data-stu-id="ccaec-119">Retail channel prerequisites</span></span>

- [<span data-ttu-id="ccaec-120">أكواد المعلومات ومجموعات أكواد المعلومات</span><span class="sxs-lookup"><span data-stu-id="ccaec-120">Info codes and info code groups</span></span>](info-codes-retail.md)
- [<span data-ttu-id="ccaec-121">إعداد ملف تعريف وظائف البيع بالتجزئة</span><span class="sxs-lookup"><span data-stu-id="ccaec-121">Set up a retail functionality profile</span></span>](retail-functionality-profile.md)
- [<span data-ttu-id="ccaec-122">إعداد دفتر عناوين للموظفين</span><span class="sxs-lookup"><span data-stu-id="ccaec-122">Set up an employee address book</span></span>](new-address-book.md)
- [<span data-ttu-id="ccaec-123">إعداد تخطيط الشاشة</span><span class="sxs-lookup"><span data-stu-id="ccaec-123">Set up a screen layout</span></span>](pos-screen-layouts.md)
- [<span data-ttu-id="ccaec-124">إعداد محطة أجهزة</span><span class="sxs-lookup"><span data-stu-id="ccaec-124">Set up a hardware station</span></span>](retail-hardware-station-configuration-installation.md)

## <a name="call-center-channel-prerequisites"></a><span data-ttu-id="ccaec-125">المتطلبات الأساسية لقناة مركز الاتصال</span><span class="sxs-lookup"><span data-stu-id="ccaec-125">Call Center channel prerequisites</span></span>

- <span data-ttu-id="ccaec-126">محددات مركز الاتصال</span><span class="sxs-lookup"><span data-stu-id="ccaec-126">Call center parameters</span></span>
- [<span data-ttu-id="ccaec-127">طريقة أمر مركز الاتصال ودفع المبلغ المسترد</span><span class="sxs-lookup"><span data-stu-id="ccaec-127">Call center order and refund payment methods</span></span>](work-with-payments.md)
- [<span data-ttu-id="ccaec-128">أوضاع تسليم مركز الاتصال والمصاريف</span><span class="sxs-lookup"><span data-stu-id="ccaec-128">Call center modes of delivery and charges</span></span>](configure-call-center-delivery.md)

## <a name="online-channel-prerequisites"></a><span data-ttu-id="ccaec-129">المتطلبات الأساسية لقناة على الإنترنت</span><span class="sxs-lookup"><span data-stu-id="ccaec-129">Online channel prerequisites</span></span>

- [<span data-ttu-id="ccaec-130">إنشاء ملف تعريف وظائف على الإنترنت</span><span class="sxs-lookup"><span data-stu-id="ccaec-130">Create an online functionality profile</span></span>](online-functionality-profile.md)

## <a name="additional-resources"></a><span data-ttu-id="ccaec-131">الموارد الإضافية</span><span class="sxs-lookup"><span data-stu-id="ccaec-131">Additional resources</span></span>

[<span data-ttu-id="ccaec-132">نظرة عامة على القنوات</span><span class="sxs-lookup"><span data-stu-id="ccaec-132">Channels overview</span></span>](channels-overview.md)

[<span data-ttu-id="ccaec-133">نظرة عامة المؤسسات والتدرجات الهرمية للمؤسسات</span><span class="sxs-lookup"><span data-stu-id="ccaec-133">Organizations and organizational hierarchies overview</span></span>](../fin-ops-core/fin-ops/organization-administration/organizations-organizational-hierarchies.md?toc=/dynamics365/commerce/toc.json)

[<span data-ttu-id="ccaec-134">إعداد التدرجات الهرمية للمؤسسات</span><span class="sxs-lookup"><span data-stu-id="ccaec-134">Set up organization hierarchies</span></span>](channels-org-hierarchies.md)

[<span data-ttu-id="ccaec-135">إنشاء كيانات قانونية</span><span class="sxs-lookup"><span data-stu-id="ccaec-135">Create legal entities</span></span>](channels-legal-entities.md)

[<span data-ttu-id="ccaec-136">إعداد قناة بيع بالتجزئة</span><span class="sxs-lookup"><span data-stu-id="ccaec-136">Set up a retail channel</span></span>](channel-setup-retail.md)
    
[<span data-ttu-id="ccaec-137">إعداد قناة عبر الإنترنت</span><span class="sxs-lookup"><span data-stu-id="ccaec-137">Set up an online channel</span></span>](channel-setup-online.md)
