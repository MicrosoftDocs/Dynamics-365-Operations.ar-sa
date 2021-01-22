---
title: إنشاء مجموعات توحيد وحسابات توحيد إضافية
description: يوضح هذا الإجراء كيفية إنشاء مجموعة حساب توحيد ثم إضافة حسابات إلى المجموعة.
author: aprilolson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LedgerConsolidateAccountGroup, MainAccountConsolidateAccount
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 826a65af563207fbfbc7391b176aa0e65b3363f9
ms.sourcegitcommit: 57e1dafa186fec77ddd8ba9425d238e36e0f0998
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 03/18/2020
ms.locfileid: "3145226"
---
# <a name="create-consolidation-groups-and-additional-consolidation-accounts"></a><span data-ttu-id="0b951-103">إنشاء مجموعات توحيد وحسابات توحيد إضافية</span><span class="sxs-lookup"><span data-stu-id="0b951-103">Create consolidation groups and additional consolidation accounts</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="0b951-104">يوضح هذا الإجراء كيفية إنشاء مجموعة حساب توحيد ثم إضافة حسابات إلى المجموعة.</span><span class="sxs-lookup"><span data-stu-id="0b951-104">This procedure shows how to create a consolidation account group and then add accounts to the group.</span></span> <span data-ttu-id="0b951-105">يستخدم هذا الإجراء شركة بيانات العرض التوضيحي USMF.</span><span class="sxs-lookup"><span data-stu-id="0b951-105">This procedure uses the demo data company USMF.</span></span>


## <a name="create-a-consolidation-account-group"></a><span data-ttu-id="0b951-106">إنشاء مجموعة حسابات مجمعة</span><span class="sxs-lookup"><span data-stu-id="0b951-106">Create a consolidation account group</span></span>
1. <span data-ttu-id="0b951-107">انتقل إلى دفتر الأستاذ العام > دليل الحسابات > الحسابات > مجموعات حسابات التوحيد.</span><span class="sxs-lookup"><span data-stu-id="0b951-107">Go to General ledger > Chart of accounts > Accounts > Consolidation account groups.</span></span>
2. <span data-ttu-id="0b951-108">انقر فوق "جديد".</span><span class="sxs-lookup"><span data-stu-id="0b951-108">Click New.</span></span>
3. <span data-ttu-id="0b951-109">في الحقل "مجموعة حساب التوحيد"، أدخل معرفًا فريدًا لمجموعة حسابات التوحيد.</span><span class="sxs-lookup"><span data-stu-id="0b951-109">In the Consolidation account group field, enter a unique identifier for the consolidation account group.</span></span>
4. <span data-ttu-id="0b951-110">في حقل "الاسم"، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="0b951-110">In the Name field, type a value.</span></span>

## <a name="add-accounts-to-consolidation-account-group"></a><span data-ttu-id="0b951-111">إضافة الحسابات لمجموعة حسابات التوحيد</span><span class="sxs-lookup"><span data-stu-id="0b951-111">Add accounts to consolidation account group</span></span>
1. <span data-ttu-id="0b951-112">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="0b951-112">Close the page.</span></span>
2. <span data-ttu-id="0b951-113">انتقل إلى دفتر الأستاذ العام > دليل الحسابات > الحسابات > حسابات التوحيد الإضافية.</span><span class="sxs-lookup"><span data-stu-id="0b951-113">Go to General ledger > Chart of accounts > Accounts > Additional consolidation accounts.</span></span>
3. <span data-ttu-id="0b951-114">انقر فوق "جديد".</span><span class="sxs-lookup"><span data-stu-id="0b951-114">Click New.</span></span>
4. <span data-ttu-id="0b951-115">في الحقل "الحساب الرئيسي"، انقر فوق زر القائمة المنسدلة لفتح البحث.</span><span class="sxs-lookup"><span data-stu-id="0b951-115">In the Main account field, click the drop-down button to open the lookup.</span></span>
5. <span data-ttu-id="0b951-116">في القائمة، انقر فوق الحساب الرئيسي الذي تريد تعيينه.</span><span class="sxs-lookup"><span data-stu-id="0b951-116">In the list, click the main account that you want to map.</span></span>
6. <span data-ttu-id="0b951-117">في الحقل "مجموعة حسابات التوحيد"، انقر فوق زر القائمة المنسدلة لفتح البحث.</span><span class="sxs-lookup"><span data-stu-id="0b951-117">In the Consolidation account group field, click the drop-down button to open the lookup.</span></span>
7. <span data-ttu-id="0b951-118">في القائمة، انقر فوق مجموعة حسابات التوحيد.</span><span class="sxs-lookup"><span data-stu-id="0b951-118">In the list, click the consolidation account group.</span></span>
8. <span data-ttu-id="0b951-119">في الحقل "حساب التوحيد"، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="0b951-119">In the Consolidation account field, type a value.</span></span>
9. <span data-ttu-id="0b951-120">في الحقل "اسم حساب التوحيد"، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="0b951-120">In the Consolidation account name field, type a value.</span></span>
