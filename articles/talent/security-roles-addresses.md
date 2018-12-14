---
title: "الوصول إلى العناوين الخاصة حسب دور الأمان"
description: "يتناول هذا الموضوع كيفية حل هذه المشكلة والتي يتعذر فيها على العميل الوصول إلى عناوين خاصة."
author: Darinkramer
manager: AnnBe
ms.date: 11/02/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-365-talent
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Talent
ms.custom: 
ms.assetid: 
ms.search.region: Global
ms.author: dkrame
ms.search.validFrom: 2018-11-02
ms.dyn365.ops.version: Talent
ms.translationtype: HT
ms.sourcegitcommit: d3f974f94b6c327fd70b8098d24f9e1f1e1e8eeb
ms.openlocfilehash: c1c1c3ce1233408e73d177f9e04f1137f3171a49
ms.contentlocale: ar-sa
ms.lasthandoff: 12/04/2018

---

# <a name="access-to-private-addresses-by-security-role"></a><span data-ttu-id="addcb-103">الوصول إلى العناوين الخاصة حسب دور الأمان</span><span class="sxs-lookup"><span data-stu-id="addcb-103">Access to private addresses by security role</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="addcb-104">**المشكلة**</span><span class="sxs-lookup"><span data-stu-id="addcb-104">**Issue**</span></span>

<span data-ttu-id="addcb-105">بعد تكرار العميل لدور أمان وتسجيل الدخول بهذا الدور الجديد، فلا يمكن للعميل الاطلاع على العناوين التي تم وضع علامة "خاص" عليها.</span><span class="sxs-lookup"><span data-stu-id="addcb-105">After a customer duplicates a security role and signs in as that new role, the customer can't see addresses that were marked as private.</span></span>

<span data-ttu-id="addcb-106">**‏‏الدقة**</span><span class="sxs-lookup"><span data-stu-id="addcb-106">**Resolution**</span></span>

<span data-ttu-id="addcb-107">لحل هذه المشكلة، يجب على العميل اتباع الخطوات التالية لدور الأمان المُكرر.</span><span class="sxs-lookup"><span data-stu-id="addcb-107">To resolve the issue, the customer must follow these steps for the duplicated security role.</span></span>

1. <span data-ttu-id="addcb-108">انتقل **إدارة المؤسسة \> دفتر العناوين العمومي \> محددات دفتر العناوين العمومية**.</span><span class="sxs-lookup"><span data-stu-id="addcb-108">Go to **Organization administration \> Global address book \> Global address book parameters**.</span></span>
2. <span data-ttu-id="addcb-109">في علامة تبويب **أمان الموقع الخاص**، قم بنقل دور الأمان الجديد من قائمة **الأدوار المتاحة** إلى قائمة **الأدوار المُحددة**.</span><span class="sxs-lookup"><span data-stu-id="addcb-109">On the **Private location security** tab, move the new security role from the **Available roles** list to the **Selected roles** list.</span></span>
3. <span data-ttu-id="addcb-110">حدد **حفظ**.</span><span class="sxs-lookup"><span data-stu-id="addcb-110">Select **Save**.</span></span>

![صفحة محددات دفتر عناوين عمومي](media/GAD-parameters.png)

