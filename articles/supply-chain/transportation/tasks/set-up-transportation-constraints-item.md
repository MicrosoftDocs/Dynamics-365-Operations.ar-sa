---
title: إعداد قيود النقل لصنف
description: سيعمل هذا الإجراء على إعداد قيد النقل لمنع نقل صنف محدد من خلال موزع محدد.
author: ShylaThompson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TMSConstraint, InventLocationIdLookup, InventItemIdLookupSimple
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 4ccd7d79fbcdd600f78dbff98ce39c04865afe37
ms.sourcegitcommit: fcb27d6a46cd544feef34f6ec7607bdd46b0c12b
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 03/18/2020
ms.locfileid: "3146136"
---
# <a name="set-up-transportation-constraints-for-an-item"></a><span data-ttu-id="5a2ca-103">إعداد قيود النقل لصنف</span><span class="sxs-lookup"><span data-stu-id="5a2ca-103">Set up transportation constraints for an item</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="5a2ca-104">سيعمل هذا الإجراء على إعداد قيد النقل لمنع نقل صنف محدد من خلال موزع محدد.</span><span class="sxs-lookup"><span data-stu-id="5a2ca-104">This procedure will set up a transportation constraint to prevent a selected item from being transported through a selected hub.</span></span> <span data-ttu-id="5a2ca-105">وعادة ما تُنفذ هذه المهمة عن طريق منسق النقل.</span><span class="sxs-lookup"><span data-stu-id="5a2ca-105">This task would typically be carried out by a Transportation coordinator.</span></span> <span data-ttu-id="5a2ca-106">يمكنك استخدام هذا الإجراء في شركة بيانات العرض التوضيحي USMF، أو في البيانات الخاصة بك.</span><span class="sxs-lookup"><span data-stu-id="5a2ca-106">You can use this procedure in the USMF demo data company or on your own data.</span></span>


## <a name="create-an-item-constaint"></a><span data-ttu-id="5a2ca-107">إنشاء قيد الصنف</span><span class="sxs-lookup"><span data-stu-id="5a2ca-107">Create an item constaint</span></span>
1. <span data-ttu-id="5a2ca-108">انتقل إلى القيود.</span><span class="sxs-lookup"><span data-stu-id="5a2ca-108">Go to Constraints.</span></span>
2. <span data-ttu-id="5a2ca-109">انقر فوق "جديد".</span><span class="sxs-lookup"><span data-stu-id="5a2ca-109">Click New.</span></span>
3. <span data-ttu-id="5a2ca-110">في الحقل "قيد الصنف" اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="5a2ca-110">In the Item constraint field, type a value.</span></span>
4. <span data-ttu-id="5a2ca-111">في حقل "الاسم"، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="5a2ca-111">In the Name field, type a value.</span></span>
5. <span data-ttu-id="5a2ca-112">في حقل "الموقع"، أدخل قيمة أو حددها.</span><span class="sxs-lookup"><span data-stu-id="5a2ca-112">In the Site field, enter or select a value.</span></span>
6. <span data-ttu-id="5a2ca-113">في الحقل "المستودع"، أدخل قيمة أو حددها.</span><span class="sxs-lookup"><span data-stu-id="5a2ca-113">In the Warehouse field, enter or select a value.</span></span>
7. <span data-ttu-id="5a2ca-114">في الحقل "رقم الصنف"، أدخل قيمة أو حددها.</span><span class="sxs-lookup"><span data-stu-id="5a2ca-114">In the Item number field, enter or select a value.</span></span>
8. <span data-ttu-id="5a2ca-115">في الحقل "الموزع"، أدخل قيمة أو حددها.</span><span class="sxs-lookup"><span data-stu-id="5a2ca-115">In the Hub field, enter or select a value.</span></span>
9. <span data-ttu-id="5a2ca-116">في الحقل "إجراء القيد"، حدد خيارًا.</span><span class="sxs-lookup"><span data-stu-id="5a2ca-116">In the Constraint action field, select an option.</span></span>
10. <span data-ttu-id="5a2ca-117">انقر فوق "حفظ".</span><span class="sxs-lookup"><span data-stu-id="5a2ca-117">Click Save.</span></span>
11. <span data-ttu-id="5a2ca-118">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="5a2ca-118">Close the page.</span></span>

