---
title: إعداد ضريبة الخصم العمومية
description: يسرد هذا الموضوع الخطوات الخاصة بإعداد ضريبة خصم عمومية للمبيعات والمشتريات.
author: roschlom
manager: AnnBe
ms.date: 01/12/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.custom: 15721
ms.assetid: b4b406fa-b772-44ec-8dd8-8eb818a921ef
ms.search.region: Global
ms.author: kailiang
ms.search.validFrom: 2020-01-12
ms.dyn365.ops.version: AX 10.0.17
ms.openlocfilehash: 7ee577651694f0553447d6e9d0851402a586f363
ms.sourcegitcommit: 630a0b3f800f36ced49b79156dd52132904fef75
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 01/25/2021
ms.locfileid: "5060695"
---
# <a name="set-up-global-withholding-tax"></a><span data-ttu-id="fb47b-103">إعداد ضريبة الخصم العمومية</span><span class="sxs-lookup"><span data-stu-id="fb47b-103">Set up global withholding tax</span></span>

<span data-ttu-id="fb47b-104">يسرد هذا الموضوع الخطوات الخاصة بإعداد ضريبة خصم عمومية للمبيعات والمشتريات.</span><span class="sxs-lookup"><span data-stu-id="fb47b-104">This topic lists the steps for setting up global withholding tax for sales and purchases.</span></span> 

1. <span data-ttu-id="fb47b-105">قم بإعداد هيئات ضريبة الخصم في صفحة **هيئات ضريبة الخصم**.</span><span class="sxs-lookup"><span data-stu-id="fb47b-105">Set up withholding tax authorities on the **Withholding tax authorities** page.</span></span>

2. <span data-ttu-id="fb47b-106">قم بإعداد فترات تسوية الخصم في صفحة **فترات تسوية ضريبة الخصم**.</span><span class="sxs-lookup"><span data-stu-id="fb47b-106">Set up withholding settlement periods on the **Withholding tax settlement periods** page.</span></span>

3. <span data-ttu-id="fb47b-107">قم بإعداد مجموعة ترحيل دفتر أستاذ الخصم في صفحة **مجموعة ترحيل دفتر الأستاذ > ضريبة الخصم**.</span><span class="sxs-lookup"><span data-stu-id="fb47b-107">Set up withholding ledger posting group on the **Withholding tax > ledger posting group** page.</span></span>

   > [!Note] 
   >
   > <span data-ttu-id="fb47b-108">سيتم تعيين حساب **ضريبة الخصم** مع حساب رئيسي **بنوع ترحيل** لضريبة الخصم.</span><span class="sxs-lookup"><span data-stu-id="fb47b-108">**Withholding tax** account will be assigned with a main account with **Posting type** of Withholding tax.</span></span> <span data-ttu-id="fb47b-109">سيتم تعيين حساب **مقاصة ضريبة الخصم** مع حساب رئيسي **بنوع ترحيل** "مقاصة ضريبة الخصم".</span><span class="sxs-lookup"><span data-stu-id="fb47b-109">**Withholding tax offset** account will also be assigned with a main account with **Posting type** "Withholding tax offset".</span></span> <span data-ttu-id="fb47b-110">انتقل إلى **دفتر الأستاذ العام > دليل الحسابات > الحسابات > الحسابات الرئيسية**، وقم بإعداد **نوع الترحيل** في النموذج الفرعي **التحقق من الترحيل** للحسابات الرئيسية.</span><span class="sxs-lookup"><span data-stu-id="fb47b-110">Go to **General ledger > Chart of accounts > Accounts > Main accounts**, set up the **Posting type** in the **Posting validation** sub-form for the main accounts.</span></span>

4. <span data-ttu-id="fb47b-111">قم بإعداد أكواد ضريبة الخصم في صفحة **أكواد ضريبة الخصم**.</span><span class="sxs-lookup"><span data-stu-id="fb47b-111">Set up withholding tax codes on the **Withholding tax codes** page.</span></span>

5. <span data-ttu-id="fb47b-112">قم بإعداد مجموعات ضريبة الخصم في صفحة **مجموعات ضريبة الخصم**.</span><span class="sxs-lookup"><span data-stu-id="fb47b-112">Set up withholding tax groups on the **Withholding tax groups** page.</span></span>

6. <span data-ttu-id="fb47b-113">قم بإعداد أنواع إيرادات ضريبة الخصم في صفحة **أنواع** **إيرادات ضريبة الخصم**.</span><span class="sxs-lookup"><span data-stu-id="fb47b-113">Set up withholding tax revenue types on the **Withholding tax revenue** **types** page.</span></span>

7. <span data-ttu-id="fb47b-114">قم بإعداد مجموعات ضريبة الخصم في صفحة **مجموعات ضريبة خصم الصنف** للصنف أو الخدمة.</span><span class="sxs-lookup"><span data-stu-id="fb47b-114">Set up withholding tax groups on the **Item withholding tax groups** page for an item or service.</span></span>

8. <span data-ttu-id="fb47b-115">قم بإعداد **الحد الأدنى لمبلغ الفاتورة** في صفحة **معلمات دفتر الأستاذ العام > ضريبة الخصم**.</span><span class="sxs-lookup"><span data-stu-id="fb47b-115">Set up **Minimum invoice amount** on the **General ledger parameters > Withholding tax** page.</span></span>
