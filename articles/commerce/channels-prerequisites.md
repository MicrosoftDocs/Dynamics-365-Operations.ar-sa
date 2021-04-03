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
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: samjar
ms.search.validFrom: 2020-01-20
ms.dyn365.ops.version: Release 10.0.8
ms.openlocfilehash: 270f751e860e56a03e20df720c088f275d0298e7
ms.sourcegitcommit: c88b54ba13a4dfe39b844ffaced4dc435560c47d
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 02/19/2021
ms.locfileid: "5477914"
---
# <a name="channel-setup-prerequisites"></a><span data-ttu-id="8cf57-103">المتطلبات الأساسية لإعداد القناة</span><span class="sxs-lookup"><span data-stu-id="8cf57-103">Channel setup prerequisites</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="8cf57-104">يقدم هذا الموضوع نظرة عامة على المتطلبات الأساسية لإعداد القناة في Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="8cf57-104">This topic presents an overview of channel setup prerequisites in Microsoft Dynamics 365 Commerce.</span></span>

<span data-ttu-id="8cf57-105">قبل أن تتمكن من إنشاء قناة Dynamics 365 Commerce، يجب إكمال العديد من المهام الأساسية.</span><span class="sxs-lookup"><span data-stu-id="8cf57-105">Before a Dynamics 365 Commerce channel can be created, several prerequisite tasks must be completed.</span></span> <span data-ttu-id="8cf57-106">يتم تنظيم القوائم التالية للمهام الأساسية حسب نوع القناة.</span><span class="sxs-lookup"><span data-stu-id="8cf57-106">The following lists of prerequisite tasks are organized by channel type.</span></span>

> [!NOTE]
> <span data-ttu-id="8cf57-107">لا تزال بعض الوثائق قيد الكتابة، وسيتم تحديث الارتباطات عند نشر محتوى جديد.</span><span class="sxs-lookup"><span data-stu-id="8cf57-107">Some documentation is still being written, and links will be updated as new content is published.</span></span>

## <a name="initialization"></a><span data-ttu-id="8cf57-108">بدء</span><span class="sxs-lookup"><span data-stu-id="8cf57-108">Initialization</span></span>

- [<span data-ttu-id="8cf57-109">تهيئة البيانات الأولية</span><span class="sxs-lookup"><span data-stu-id="8cf57-109">Initialize seed data</span></span>](enable-configure-retail-functionality.md)

## <a name="global-prerequisities-required-for-all-channel-types"></a><span data-ttu-id="8cf57-110">المتطلبات الأساسية العمومية لكل أنواع القنوات</span><span class="sxs-lookup"><span data-stu-id="8cf57-110">Global prerequisities required for all channel types</span></span>

- [<span data-ttu-id="8cf57-111">تعريف بنية الكيان القانوني وتكوينها</span><span class="sxs-lookup"><span data-stu-id="8cf57-111">Define and configure your legal entity structure</span></span>](channels-legal-entities.md) 
- [<span data-ttu-id="8cf57-112">تكوين التدرج الهرمي للمؤسسات</span><span class="sxs-lookup"><span data-stu-id="8cf57-112">Configure your organizational hierarchy</span></span>](channels-org-hierarchies.md)
- [<span data-ttu-id="8cf57-113">إعداد مستودع</span><span class="sxs-lookup"><span data-stu-id="8cf57-113">Set up a warehouse</span></span>](channels-setup-warehouse.md)
- [<span data-ttu-id="8cf57-114">تكوين ضريبة المبيعات</span><span class="sxs-lookup"><span data-stu-id="8cf57-114">Configure sales tax</span></span>](../finance/general-ledger/indirect-taxes-overview.md?toc=/dynamics365/commerce/toc.json)
- [<span data-ttu-id="8cf57-115">إعداد ملف تعريف إخطار البريد الإلكتروني</span><span class="sxs-lookup"><span data-stu-id="8cf57-115">Set up an email notification profile</span></span>](email-notification-profiles.md)
- [<span data-ttu-id="8cf57-116">إعداد التسلسلات الرقمية</span><span class="sxs-lookup"><span data-stu-id="8cf57-116">Set up number sequences</span></span>](../fin-ops-core/fin-ops/organization-administration/number-sequence-overview.md?toc=/dynamics365/commerce/toc.json)
- [<span data-ttu-id="8cf57-117">إعداد عميل ودفتر عناوين افتراضيين</span><span class="sxs-lookup"><span data-stu-id="8cf57-117">Set up a default customer and address book</span></span>](default-customer.md)
<!--
- [Configure commerce parameters](commerce-parameters.md)
-->

## <a name="retail-channel-prerequisites"></a><span data-ttu-id="8cf57-118">المتطلبات الأساسية‬ لقناة البيع بالتجزئة</span><span class="sxs-lookup"><span data-stu-id="8cf57-118">Retail channel prerequisites</span></span>

- [<span data-ttu-id="8cf57-119">أكواد المعلومات ومجموعات أكواد المعلومات</span><span class="sxs-lookup"><span data-stu-id="8cf57-119">Info codes and info code groups</span></span>](info-codes-retail.md)
- [<span data-ttu-id="8cf57-120">إعداد ملف تعريف وظائف البيع بالتجزئة</span><span class="sxs-lookup"><span data-stu-id="8cf57-120">Set up a retail functionality profile</span></span>](retail-functionality-profile.md)
- [<span data-ttu-id="8cf57-121">إعداد دفتر عناوين للموظفين</span><span class="sxs-lookup"><span data-stu-id="8cf57-121">Set up an employee address book</span></span>](new-address-book.md)
- [<span data-ttu-id="8cf57-122">إعداد تخطيط الشاشة</span><span class="sxs-lookup"><span data-stu-id="8cf57-122">Set up a screen layout</span></span>](pos-screen-layouts.md)
- [<span data-ttu-id="8cf57-123">إعداد محطة أجهزة</span><span class="sxs-lookup"><span data-stu-id="8cf57-123">Set up a hardware station</span></span>](retail-hardware-station-configuration-installation.md)

## <a name="call-center-channel-prerequisites"></a><span data-ttu-id="8cf57-124">المتطلبات الأساسية لقناة مركز الاتصال</span><span class="sxs-lookup"><span data-stu-id="8cf57-124">Call Center channel prerequisites</span></span>

- <span data-ttu-id="8cf57-125">محددات مركز الاتصال</span><span class="sxs-lookup"><span data-stu-id="8cf57-125">Call center parameters</span></span>
- [<span data-ttu-id="8cf57-126">طريقة أمر مركز الاتصال ودفع المبلغ المسترد</span><span class="sxs-lookup"><span data-stu-id="8cf57-126">Call center order and refund payment methods</span></span>](work-with-payments.md)
- [<span data-ttu-id="8cf57-127">أوضاع تسليم مركز الاتصال والمصاريف</span><span class="sxs-lookup"><span data-stu-id="8cf57-127">Call center modes of delivery and charges</span></span>](configure-call-center-delivery.md)

## <a name="online-channel-prerequisites"></a><span data-ttu-id="8cf57-128">المتطلبات الأساسية لقناة على الإنترنت</span><span class="sxs-lookup"><span data-stu-id="8cf57-128">Online channel prerequisites</span></span>

- [<span data-ttu-id="8cf57-129">إنشاء ملف تعريف وظائف على الإنترنت</span><span class="sxs-lookup"><span data-stu-id="8cf57-129">Create an online functionality profile</span></span>](online-functionality-profile.md)

## <a name="additional-resources"></a><span data-ttu-id="8cf57-130">الموارد الإضافية</span><span class="sxs-lookup"><span data-stu-id="8cf57-130">Additional resources</span></span>

[<span data-ttu-id="8cf57-131">نظرة عامة على القنوات</span><span class="sxs-lookup"><span data-stu-id="8cf57-131">Channels overview</span></span>](channels-overview.md)

[<span data-ttu-id="8cf57-132">نظرة عامة المؤسسات والتدرجات الهرمية للمؤسسات</span><span class="sxs-lookup"><span data-stu-id="8cf57-132">Organizations and organizational hierarchies overview</span></span>](../fin-ops-core/fin-ops/organization-administration/organizations-organizational-hierarchies.md?toc=/dynamics365/commerce/toc.json)

[<span data-ttu-id="8cf57-133">إعداد التدرجات الهرمية للمؤسسات</span><span class="sxs-lookup"><span data-stu-id="8cf57-133">Set up organization hierarchies</span></span>](channels-org-hierarchies.md)

[<span data-ttu-id="8cf57-134">إنشاء كيانات قانونية</span><span class="sxs-lookup"><span data-stu-id="8cf57-134">Create legal entities</span></span>](channels-legal-entities.md)

[<span data-ttu-id="8cf57-135">إعداد قناة بيع بالتجزئة</span><span class="sxs-lookup"><span data-stu-id="8cf57-135">Set up a retail channel</span></span>](channel-setup-retail.md)
    
[<span data-ttu-id="8cf57-136">إعداد قناة عبر الإنترنت</span><span class="sxs-lookup"><span data-stu-id="8cf57-136">Set up an online channel</span></span>](channel-setup-online.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
