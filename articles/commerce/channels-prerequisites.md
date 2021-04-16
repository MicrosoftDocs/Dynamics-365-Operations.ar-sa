---
title: المتطلبات الأساسية‬ لإعداد قناة
description: يقدم هذا الموضوع نظرة عامة على المتطلبات الأساسية لإعداد القناة في Microsoft Dynamics 365 Commerce.
author: samjarawan
ms.date: 02/21/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: samjar
ms.search.validFrom: 2020-01-20
ms.dyn365.ops.version: Release 10.0.8
ms.openlocfilehash: 33fcead6c0b08db17f24b638376a23b8b6024a5b
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 03/31/2021
ms.locfileid: "5800509"
---
# <a name="channel-setup-prerequisites"></a><span data-ttu-id="c913c-103">المتطلبات الأساسية لإعداد القناة</span><span class="sxs-lookup"><span data-stu-id="c913c-103">Channel setup prerequisites</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="c913c-104">يقدم هذا الموضوع نظرة عامة على المتطلبات الأساسية لإعداد القناة في Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="c913c-104">This topic presents an overview of channel setup prerequisites in Microsoft Dynamics 365 Commerce.</span></span>

<span data-ttu-id="c913c-105">قبل أن تتمكن من إنشاء قناة Dynamics 365 Commerce، يجب إكمال العديد من المهام الأساسية.</span><span class="sxs-lookup"><span data-stu-id="c913c-105">Before a Dynamics 365 Commerce channel can be created, several prerequisite tasks must be completed.</span></span> <span data-ttu-id="c913c-106">يتم تنظيم القوائم التالية للمهام الأساسية حسب نوع القناة.</span><span class="sxs-lookup"><span data-stu-id="c913c-106">The following lists of prerequisite tasks are organized by channel type.</span></span>

> [!NOTE]
> <span data-ttu-id="c913c-107">لا تزال بعض الوثائق قيد الكتابة، وسيتم تحديث الارتباطات عند نشر محتوى جديد.</span><span class="sxs-lookup"><span data-stu-id="c913c-107">Some documentation is still being written, and links will be updated as new content is published.</span></span>

## <a name="initialization"></a><span data-ttu-id="c913c-108">بدء</span><span class="sxs-lookup"><span data-stu-id="c913c-108">Initialization</span></span>

- [<span data-ttu-id="c913c-109">تهيئة البيانات الأولية</span><span class="sxs-lookup"><span data-stu-id="c913c-109">Initialize seed data</span></span>](enable-configure-retail-functionality.md)

## <a name="global-prerequisities-required-for-all-channel-types"></a><span data-ttu-id="c913c-110">المتطلبات الأساسية العمومية لكل أنواع القنوات</span><span class="sxs-lookup"><span data-stu-id="c913c-110">Global prerequisities required for all channel types</span></span>

- [<span data-ttu-id="c913c-111">تعريف بنية الكيان القانوني وتكوينها</span><span class="sxs-lookup"><span data-stu-id="c913c-111">Define and configure your legal entity structure</span></span>](channels-legal-entities.md) 
- [<span data-ttu-id="c913c-112">تكوين التدرج الهرمي للمؤسسات</span><span class="sxs-lookup"><span data-stu-id="c913c-112">Configure your organizational hierarchy</span></span>](channels-org-hierarchies.md)
- [<span data-ttu-id="c913c-113">إعداد مستودع</span><span class="sxs-lookup"><span data-stu-id="c913c-113">Set up a warehouse</span></span>](channels-setup-warehouse.md)
- [<span data-ttu-id="c913c-114">تكوين ضريبة المبيعات</span><span class="sxs-lookup"><span data-stu-id="c913c-114">Configure sales tax</span></span>](../finance/general-ledger/indirect-taxes-overview.md?toc=/dynamics365/commerce/toc.json)
- [<span data-ttu-id="c913c-115">إعداد ملف تعريف إخطار البريد الإلكتروني</span><span class="sxs-lookup"><span data-stu-id="c913c-115">Set up an email notification profile</span></span>](email-notification-profiles.md)
- [<span data-ttu-id="c913c-116">إعداد التسلسلات الرقمية</span><span class="sxs-lookup"><span data-stu-id="c913c-116">Set up number sequences</span></span>](../fin-ops-core/fin-ops/organization-administration/number-sequence-overview.md?toc=/dynamics365/commerce/toc.json)
- [<span data-ttu-id="c913c-117">إعداد عميل ودفتر عناوين افتراضيين</span><span class="sxs-lookup"><span data-stu-id="c913c-117">Set up a default customer and address book</span></span>](default-customer.md)
<!--
- [Configure commerce parameters](commerce-parameters.md)
-->

## <a name="retail-channel-prerequisites"></a><span data-ttu-id="c913c-118">المتطلبات الأساسية‬ لقناة البيع بالتجزئة</span><span class="sxs-lookup"><span data-stu-id="c913c-118">Retail channel prerequisites</span></span>

- [<span data-ttu-id="c913c-119">أكواد المعلومات ومجموعات أكواد المعلومات</span><span class="sxs-lookup"><span data-stu-id="c913c-119">Info codes and info code groups</span></span>](info-codes-retail.md)
- [<span data-ttu-id="c913c-120">إعداد ملف تعريف وظائف البيع بالتجزئة</span><span class="sxs-lookup"><span data-stu-id="c913c-120">Set up a retail functionality profile</span></span>](retail-functionality-profile.md)
- [<span data-ttu-id="c913c-121">إعداد دفتر عناوين للموظفين</span><span class="sxs-lookup"><span data-stu-id="c913c-121">Set up an employee address book</span></span>](new-address-book.md)
- [<span data-ttu-id="c913c-122">إعداد تخطيط الشاشة</span><span class="sxs-lookup"><span data-stu-id="c913c-122">Set up a screen layout</span></span>](pos-screen-layouts.md)
- [<span data-ttu-id="c913c-123">إعداد محطة أجهزة</span><span class="sxs-lookup"><span data-stu-id="c913c-123">Set up a hardware station</span></span>](retail-hardware-station-configuration-installation.md)

## <a name="call-center-channel-prerequisites"></a><span data-ttu-id="c913c-124">المتطلبات الأساسية لقناة مركز الاتصال</span><span class="sxs-lookup"><span data-stu-id="c913c-124">Call Center channel prerequisites</span></span>

- <span data-ttu-id="c913c-125">محددات مركز الاتصال</span><span class="sxs-lookup"><span data-stu-id="c913c-125">Call center parameters</span></span>
- [<span data-ttu-id="c913c-126">طريقة أمر مركز الاتصال ودفع المبلغ المسترد</span><span class="sxs-lookup"><span data-stu-id="c913c-126">Call center order and refund payment methods</span></span>](work-with-payments.md)
- [<span data-ttu-id="c913c-127">أوضاع تسليم مركز الاتصال والمصاريف</span><span class="sxs-lookup"><span data-stu-id="c913c-127">Call center modes of delivery and charges</span></span>](configure-call-center-delivery.md)

## <a name="online-channel-prerequisites"></a><span data-ttu-id="c913c-128">المتطلبات الأساسية لقناة على الإنترنت</span><span class="sxs-lookup"><span data-stu-id="c913c-128">Online channel prerequisites</span></span>

- [<span data-ttu-id="c913c-129">إنشاء ملف تعريف وظائف على الإنترنت</span><span class="sxs-lookup"><span data-stu-id="c913c-129">Create an online functionality profile</span></span>](online-functionality-profile.md)

## <a name="additional-resources"></a><span data-ttu-id="c913c-130">الموارد الإضافية</span><span class="sxs-lookup"><span data-stu-id="c913c-130">Additional resources</span></span>

[<span data-ttu-id="c913c-131">نظرة عامة على القنوات</span><span class="sxs-lookup"><span data-stu-id="c913c-131">Channels overview</span></span>](channels-overview.md)

[<span data-ttu-id="c913c-132">نظرة عامة المؤسسات والتدرجات الهرمية للمؤسسات</span><span class="sxs-lookup"><span data-stu-id="c913c-132">Organizations and organizational hierarchies overview</span></span>](../fin-ops-core/fin-ops/organization-administration/organizations-organizational-hierarchies.md?toc=/dynamics365/commerce/toc.json)

[<span data-ttu-id="c913c-133">إعداد التدرجات الهرمية للمؤسسات</span><span class="sxs-lookup"><span data-stu-id="c913c-133">Set up organization hierarchies</span></span>](channels-org-hierarchies.md)

[<span data-ttu-id="c913c-134">إنشاء كيانات قانونية</span><span class="sxs-lookup"><span data-stu-id="c913c-134">Create legal entities</span></span>](channels-legal-entities.md)

[<span data-ttu-id="c913c-135">إعداد قناة بيع بالتجزئة</span><span class="sxs-lookup"><span data-stu-id="c913c-135">Set up a retail channel</span></span>](channel-setup-retail.md)
    
[<span data-ttu-id="c913c-136">إعداد قناة عبر الإنترنت</span><span class="sxs-lookup"><span data-stu-id="c913c-136">Set up an online channel</span></span>](channel-setup-online.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
