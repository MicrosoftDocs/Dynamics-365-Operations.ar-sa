---
title: البحث عن الموردين
description: تعلَّم كيفية البحث عن الموردين حسب معايير محددة.
author: mkirknel
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: VendSearchCriterion, VendSearchAddCategory, VendSearchAddReviewCriterionGroup, VendSearchResults, VendSearchAddReviewCriterion
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: bc28deb979fe8dc4e31befe6d4d5f6f91388f13e
ms.sourcegitcommit: 827d77c638555396b32d36af5d22d1b61dafb0e8
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 10/16/2020
ms.locfileid: "4421795"
---
# <a name="search-for-vendors"></a><span data-ttu-id="dec9b-103">البحث عن الموردين</span><span class="sxs-lookup"><span data-stu-id="dec9b-103">Search for vendors</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="dec9b-104">تعلَّم كيفية البحث عن الموردين حسب معايير محددة.</span><span class="sxs-lookup"><span data-stu-id="dec9b-104">Learn how to search for vendors based on specific criteria.</span></span> <span data-ttu-id="dec9b-105">يوضح هذا المثال لك كيفية البحث عن الموردين المعتمدين لفئة معينة من التدبير والحصول على عناوينهم الرئيسية في بلد معين.</span><span class="sxs-lookup"><span data-stu-id="dec9b-105">This example shows you how to search for vendors that are approved for a particular procurement category and have their primary address in a specific country.</span></span> <span data-ttu-id="dec9b-106">يمكنك تنفيذ هذا الإجراء في شركة بيانات العرض التقديمي USMF، أو في البيانات الخاصة بك.</span><span class="sxs-lookup"><span data-stu-id="dec9b-106">You can run this procedure in demo data company USMF, or on your own data.</span></span> <span data-ttu-id="dec9b-107">عادة ما يتم تنفيذ هذه المهمة بواسطة موظف تدبير محترف.</span><span class="sxs-lookup"><span data-stu-id="dec9b-107">This task would usually be carried out by a procurement professional.</span></span>

1. <span data-ttu-id="dec9b-108">انتقل إلى التدبير والتوريد > الموردون > البحث عن الموردين.</span><span class="sxs-lookup"><span data-stu-id="dec9b-108">Go to Procurement and sourcing > Vendors > Vendor search.</span></span>
2. <span data-ttu-id="dec9b-109">انقر فوق رمز الجمع لفتح صفحة تحديد فئة التدبير.</span><span class="sxs-lookup"><span data-stu-id="dec9b-109">Click on the Plus icon to open the Procurement category selection page.</span></span>  
3. <span data-ttu-id="dec9b-110">في الشجرة، حدد "فئات التدبير للشركة لأجهزة الشركة/المكتب".</span><span class="sxs-lookup"><span data-stu-id="dec9b-110">In the tree, select 'CORP PROCUREMENT CATEGORIES\OFFICE MACHINES'.</span></span>
    * <span data-ttu-id="dec9b-111">إذا كنت تنفذ هذا الإجراء كدليل مهمة، فقد تضطر إلى النقر فوق الزر "إلغاء التأمين" قبل أن تتمكن من تحديد العقدة الصحيحة.</span><span class="sxs-lookup"><span data-stu-id="dec9b-111">If you're running this procedure as a task guide, you may have to click the Unlock button before you can select the correct node.</span></span> <span data-ttu-id="dec9b-112">إذا كنت لا تستخدم USMF، فحدد إحدى الفئات المتوفرة لديك.</span><span class="sxs-lookup"><span data-stu-id="dec9b-112">If you're not using USMF, select one of the categories that you have.</span></span>  
4. <span data-ttu-id="dec9b-113">وانقر فوق إضافة.</span><span class="sxs-lookup"><span data-stu-id="dec9b-113">Click Add.</span></span>
    * <span data-ttu-id="dec9b-114">من الممكن تحديد أكثر من فئة واحدة هنا.</span><span class="sxs-lookup"><span data-stu-id="dec9b-114">It's possible to select more than one category here.</span></span> <span data-ttu-id="dec9b-115">إذا قمت بذلك، ستحصل في نتيجة البحث على جميع الموردين الذين تم اعتمادهم لفئة واحدة على الأقل.</span><span class="sxs-lookup"><span data-stu-id="dec9b-115">If you do so, the search will find all the vendors that are approved for at least one of the categories.</span></span>  
5. <span data-ttu-id="dec9b-116">انقر فوق "موافق".</span><span class="sxs-lookup"><span data-stu-id="dec9b-116">Click OK.</span></span>
6. <span data-ttu-id="dec9b-117">في الحقل "البلد/المنطقة"، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="dec9b-117">In the Country/region field, type a value.</span></span>
7. <span data-ttu-id="dec9b-118">انقر فوق "موافق".</span><span class="sxs-lookup"><span data-stu-id="dec9b-118">Click OK.</span></span>

