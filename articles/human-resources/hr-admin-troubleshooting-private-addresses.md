---
title: الوصول إلى العناوين الخاصة حسب دور الأمان
description: يتناول هذا المقال كيفية حل هذه المشكلة والتي يتعذر فيها على العميل الوصول إلى عناوين خاصة.
author: andreabichsel
manager: AnnBe
ms.date: 11/02/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-human-resources
ms.technology: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2018-11-02
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: facfd17f007b2c9e6f068d0ec4c5ce45b85a1b78
ms.sourcegitcommit: 40163705a134c9874fd33be80c7ae59ccce22c21
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 02/03/2020
ms.locfileid: "3007982"
---
# <a name="access-to-private-addresses-by-security-role"></a><span data-ttu-id="e95a1-103">الوصول إلى العناوين الخاصة حسب دور الأمان</span><span class="sxs-lookup"><span data-stu-id="e95a1-103">Access to private addresses by security role</span></span>

<span data-ttu-id="e95a1-104">**المشكلة**</span><span class="sxs-lookup"><span data-stu-id="e95a1-104">**Issue**</span></span>

<span data-ttu-id="e95a1-105">بعد تكرار العميل لدور أمان وتسجيل الدخول بهذا الدور الجديد، فلا يمكن للعميل الاطلاع على العناوين التي تم وضع علامة "خاص" عليها.</span><span class="sxs-lookup"><span data-stu-id="e95a1-105">After a customer duplicates a security role and signs in as that new role, the customer can't see addresses that were marked as private.</span></span>

<span data-ttu-id="e95a1-106">**‏‏الدقة**</span><span class="sxs-lookup"><span data-stu-id="e95a1-106">**Resolution**</span></span>

<span data-ttu-id="e95a1-107">لحل هذه المشكلة، يجب على العميل اتباع الخطوات التالية لدور الأمان المُكرر.</span><span class="sxs-lookup"><span data-stu-id="e95a1-107">To resolve the issue, the customer must follow these steps for the duplicated security role.</span></span>

1. <span data-ttu-id="e95a1-108">انتقل **إدارة المؤسسة \> دفتر العناوين العمومي \> محددات دفتر العناوين العمومية**.</span><span class="sxs-lookup"><span data-stu-id="e95a1-108">Go to **Organization administration \> Global address book \> Global address book parameters**.</span></span>
2. <span data-ttu-id="e95a1-109">في علامة تبويب **أمان الموقع الخاص**، قم بنقل دور الأمان الجديد من قائمة **الأدوار المتاحة** إلى قائمة **الأدوار المُحددة**.</span><span class="sxs-lookup"><span data-stu-id="e95a1-109">On the **Private location security** tab, move the new security role from the **Available roles** list to the **Selected roles** list.</span></span>
3. <span data-ttu-id="e95a1-110">حدد **حفظ**.</span><span class="sxs-lookup"><span data-stu-id="e95a1-110">Select **Save**.</span></span>

![صفحة محددات دفتر عناوين عمومي](media/GAD-parameters.png)
