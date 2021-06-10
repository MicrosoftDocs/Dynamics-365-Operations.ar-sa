---
title: الوصول إلى العناوين الخاصة حسب دور الأمان
description: يتناول هذا المقال كيفية حل هذه المشكلة والتي يتعذر فيها على العميل الوصول إلى عناوين خاصة.
author: andreabichsel
ms.date: 11/02/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.search.scope: Human Resources
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2018-11-02
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 2edcef338f0ff8fcf231d4314fc972284397d000
ms.sourcegitcommit: 879ee8a10e6158885795dce4b3db5077540eec41
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 05/18/2021
ms.locfileid: "6053313"
---
# <a name="access-to-private-addresses-by-security-role"></a><span data-ttu-id="8fcfd-103">الوصول إلى العناوين الخاصة حسب دور الأمان</span><span class="sxs-lookup"><span data-stu-id="8fcfd-103">Access to private addresses by security role</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="8fcfd-104">**المشكلة**</span><span class="sxs-lookup"><span data-stu-id="8fcfd-104">**Issue**</span></span>

<span data-ttu-id="8fcfd-105">بعد تكرار العميل لدور أمان وتسجيل الدخول بهذا الدور الجديد، فلا يمكن للعميل الاطلاع على العناوين التي تم وضع علامة "خاص" عليها.</span><span class="sxs-lookup"><span data-stu-id="8fcfd-105">After a customer duplicates a security role and signs in as that new role, the customer can't see addresses that were marked as private.</span></span>

<span data-ttu-id="8fcfd-106">**‏‏الدقة**</span><span class="sxs-lookup"><span data-stu-id="8fcfd-106">**Resolution**</span></span>

<span data-ttu-id="8fcfd-107">لحل هذه المشكلة، يجب على العميل اتباع الخطوات التالية لدور الأمان المُكرر.</span><span class="sxs-lookup"><span data-stu-id="8fcfd-107">To resolve the issue, the customer must follow these steps for the duplicated security role.</span></span>

1. <span data-ttu-id="8fcfd-108">انتقل **إدارة المؤسسة \> دفتر العناوين العمومي \> محددات دفتر العناوين العمومية**.</span><span class="sxs-lookup"><span data-stu-id="8fcfd-108">Go to **Organization administration \> Global address book \> Global address book parameters**.</span></span>
2. <span data-ttu-id="8fcfd-109">في علامة تبويب **أمان الموقع الخاص**، قم بنقل دور الأمان الجديد من قائمة **الأدوار المتاحة** إلى قائمة **الأدوار المُحددة**.</span><span class="sxs-lookup"><span data-stu-id="8fcfd-109">On the **Private location security** tab, move the new security role from the **Available roles** list to the **Selected roles** list.</span></span>
3. <span data-ttu-id="8fcfd-110">حدد **حفظ**.</span><span class="sxs-lookup"><span data-stu-id="8fcfd-110">Select **Save**.</span></span>

![صفحة محددات دفتر عناوين عمومي](media/GAD-parameters.png)


[!INCLUDE[footer-include](../includes/footer-banner.md)]