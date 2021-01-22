---
title: مجموعات ائتمان العملاء
description: يوفر هذا الموضوع معلومات حول مجموعات ائتمان العملاء.
author: mikefalkner
manager: AnnBe
ms.date: 04/14/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: roschloma
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: roschlom
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: 1ddf41d88d085b102a7d69eeeff0ec463d8b4137
ms.sourcegitcommit: 708ca25687a4e48271cdcd6d2d22d99fb94cf140
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 10/10/2020
ms.locfileid: "3977949"
---
# <a name="customer-credit-groups"></a><span data-ttu-id="2d6ef-103">مجموعات الائتمان للعميل</span><span class="sxs-lookup"><span data-stu-id="2d6ef-103">Customer credit groups</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="2d6ef-104">يمكنك تحديد مجموعات من العملاء لديهم حدًا ائتمانيًا مشتركًا.</span><span class="sxs-lookup"><span data-stu-id="2d6ef-104">You can define groups of customers who have a shared credit limit.</span></span> <span data-ttu-id="2d6ef-105">وتتم أيضًا مراعاة الحد الائتماني الفردي المحدد في حساب فاتورة العميل.</span><span class="sxs-lookup"><span data-stu-id="2d6ef-105">The individual credit limit that is defined on the customer invoice account is also considered.</span></span>

<span data-ttu-id="2d6ef-106">يمكن تحديد أعضاء مجموعة ائتمان العملاء من كيانات قانونية مختلفة.</span><span class="sxs-lookup"><span data-stu-id="2d6ef-106">Members of a customer credit group can be selected from different legal entities.</span></span> <span data-ttu-id="2d6ef-107">عند إضافة عميل إلى قائمة العملاء في مجموعة ائتمان العملاء، يتغير تاريخ انتهاء صلاحية الحد الائتماني لكل عميل إلى تاريخ انتهاء الصلاحية المعين للمجموعة.</span><span class="sxs-lookup"><span data-stu-id="2d6ef-107">When you add a customer to the list of customers in the customer credit group, the expiration date of the credit limit for each customer is changed to the expiration date that is assigned to the group.</span></span>

<span data-ttu-id="2d6ef-108">يمكنك إعداد مجموعات ائتمان العملاء في صفحة **مجموعات ائتمان العملاء** ( **إدارة الائتمان \> مجموعات ائتمان العملاء \> مجموعات ائتمان العملاء** ).</span><span class="sxs-lookup"><span data-stu-id="2d6ef-108">You can set up customer credit groups on the **Customer credit groups** page ( **Credit management \> Customer credit groups \> Customer credit groups** ).</span></span>

1. <span data-ttu-id="2d6ef-109">في الحقلين‏‎ **رقم المجموعة** و **الوصف** ، أدخل معرفًا ووصفًا للمجموعة.</span><span class="sxs-lookup"><span data-stu-id="2d6ef-109">In the **Group number** and **Description** fields, enter an identifier and description for the group.</span></span>
2. <span data-ttu-id="2d6ef-110">في الحقلين‏‎ **الحد الائتماني** و **العملة** ، أدخل الحد الائتماني‏‎ والعملة التي ينبغي استخدامها عندما يتحقق النظام من الحد الائتماني لأي عضو في المجموعة.</span><span class="sxs-lookup"><span data-stu-id="2d6ef-110">In the **Credit limit** and **Currency** fields, enter the credit limit and currency that should be used when the system checks the credit limit for any member of the group.</span></span>
3. <span data-ttu-id="2d6ef-111">في الحقل **حد ائتماني حتى تاريخ** ، أدخل التاريخ الذي تنتهي فيه صلاحية الحد الائتماني.</span><span class="sxs-lookup"><span data-stu-id="2d6ef-111">In the **Credit limit to date** field, enter the date when the credit limit expires.</span></span> <span data-ttu-id="2d6ef-112">يجب تعيين تاريخ انتهاء صلاحية لمجموعات ائتمان العملاء.</span><span class="sxs-lookup"><span data-stu-id="2d6ef-112">Customer credit groups must have an expiration date.</span></span>

<span data-ttu-id="2d6ef-113">بعد الانتهاء من إعداد مجموعة ائتمان العملاء، يمكنك إضافة العملاء إليها عن طريق تحديد كيانهم القانوني ومعرف حساب العميل الخاص بكل واحد منهم.</span><span class="sxs-lookup"><span data-stu-id="2d6ef-113">After you've finished setting up a customer credit group, you can add customers to it by specifying their legal entity and customer account ID.</span></span> <span data-ttu-id="2d6ef-114">عند إضافة عميل جديد إلى مجموعة ائتمان العملاء، يبحث النظام عن العميل نفسه عبر جميع الكيانات القانونية ويطالبك بإضافته إلى مجموعة ائتمان العملاء.</span><span class="sxs-lookup"><span data-stu-id="2d6ef-114">When you add a new customer to a customer credit group, the system searches for the same customer account across all legal entities and prompts you to add it to the customer credit group.</span></span>

<span data-ttu-id="2d6ef-115">استخدم قائمة **الأرصدة القديمة‬** لعرض تفاصيل رصيد قديم لجميع فواتير العملاء في مجموعة ائتمان العملاء.</span><span class="sxs-lookup"><span data-stu-id="2d6ef-115">Use the **Aged balances** menu to view the details of the aging balance for all invoice customers in a customer credit group.</span></span> <span data-ttu-id="2d6ef-116">تعرض صفحة‏‎ **رصيد التقادم** ملخصًا للأرصدة القديمة الخاصة بحسابات عملاء الفواتير.</span><span class="sxs-lookup"><span data-stu-id="2d6ef-116">The **Aging balance** page shows a summary of the aged balances for the invoice customer accounts.</span></span>