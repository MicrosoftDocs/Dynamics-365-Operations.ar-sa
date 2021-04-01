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
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: a02d6cf5516e63378f4aa356627c069404546e07
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 02/15/2021
ms.locfileid: "5216493"
---
# <a name="create-consolidation-groups-and-additional-consolidation-accounts"></a><span data-ttu-id="ad76f-103">إنشاء مجموعات توحيد وحسابات توحيد إضافية</span><span class="sxs-lookup"><span data-stu-id="ad76f-103">Create consolidation groups and additional consolidation accounts</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="ad76f-104">يوضح هذا الإجراء كيفية إنشاء مجموعة حساب توحيد ثم إضافة حسابات إلى المجموعة.</span><span class="sxs-lookup"><span data-stu-id="ad76f-104">This procedure shows how to create a consolidation account group and then add accounts to the group.</span></span> <span data-ttu-id="ad76f-105">يستخدم هذا الإجراء شركة بيانات العرض التوضيحي USMF.</span><span class="sxs-lookup"><span data-stu-id="ad76f-105">This procedure uses the demo data company USMF.</span></span>


## <a name="create-a-consolidation-account-group"></a><span data-ttu-id="ad76f-106">إنشاء مجموعة حسابات مجمعة</span><span class="sxs-lookup"><span data-stu-id="ad76f-106">Create a consolidation account group</span></span>
1. <span data-ttu-id="ad76f-107">انتقل إلى دفتر الأستاذ العام > دليل الحسابات > الحسابات > مجموعات حسابات التوحيد.</span><span class="sxs-lookup"><span data-stu-id="ad76f-107">Go to General ledger > Chart of accounts > Accounts > Consolidation account groups.</span></span>
2. <span data-ttu-id="ad76f-108">انقر فوق "جديد".</span><span class="sxs-lookup"><span data-stu-id="ad76f-108">Click New.</span></span>
3. <span data-ttu-id="ad76f-109">في الحقل "مجموعة حساب التوحيد"، أدخل معرفًا فريدًا لمجموعة حسابات التوحيد.</span><span class="sxs-lookup"><span data-stu-id="ad76f-109">In the Consolidation account group field, enter a unique identifier for the consolidation account group.</span></span>
4. <span data-ttu-id="ad76f-110">في حقل "الاسم"، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="ad76f-110">In the Name field, type a value.</span></span>

## <a name="add-accounts-to-consolidation-account-group"></a><span data-ttu-id="ad76f-111">إضافة الحسابات لمجموعة حسابات التوحيد</span><span class="sxs-lookup"><span data-stu-id="ad76f-111">Add accounts to consolidation account group</span></span>
1. <span data-ttu-id="ad76f-112">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="ad76f-112">Close the page.</span></span>
2. <span data-ttu-id="ad76f-113">انتقل إلى دفتر الأستاذ العام > دليل الحسابات > الحسابات > حسابات التوحيد الإضافية.</span><span class="sxs-lookup"><span data-stu-id="ad76f-113">Go to General ledger > Chart of accounts > Accounts > Additional consolidation accounts.</span></span>
3. <span data-ttu-id="ad76f-114">انقر فوق "جديد".</span><span class="sxs-lookup"><span data-stu-id="ad76f-114">Click New.</span></span>
4. <span data-ttu-id="ad76f-115">في الحقل "الحساب الرئيسي"، انقر فوق زر القائمة المنسدلة لفتح البحث.</span><span class="sxs-lookup"><span data-stu-id="ad76f-115">In the Main account field, click the drop-down button to open the lookup.</span></span>
5. <span data-ttu-id="ad76f-116">في القائمة، انقر فوق الحساب الرئيسي الذي تريد تعيينه.</span><span class="sxs-lookup"><span data-stu-id="ad76f-116">In the list, click the main account that you want to map.</span></span>
6. <span data-ttu-id="ad76f-117">في الحقل "مجموعة حسابات التوحيد"، انقر فوق زر القائمة المنسدلة لفتح البحث.</span><span class="sxs-lookup"><span data-stu-id="ad76f-117">In the Consolidation account group field, click the drop-down button to open the lookup.</span></span>
7. <span data-ttu-id="ad76f-118">في القائمة، انقر فوق مجموعة حسابات التوحيد.</span><span class="sxs-lookup"><span data-stu-id="ad76f-118">In the list, click the consolidation account group.</span></span>
8. <span data-ttu-id="ad76f-119">في الحقل "حساب التوحيد"، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="ad76f-119">In the Consolidation account field, type a value.</span></span>
9. <span data-ttu-id="ad76f-120">في الحقل "اسم حساب التوحيد"، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="ad76f-120">In the Consolidation account name field, type a value.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]