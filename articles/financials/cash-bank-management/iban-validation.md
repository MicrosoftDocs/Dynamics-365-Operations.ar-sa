---
title: إدارة التحقق من صحة حساب رقم الحساب البنكي الدولي (IBAN)
description: يشرح هذا الموضوع كيفية إدارة التحقق من صحة حساب رقم الحساب البنكي الدولي (IBAN).
author: mikefalkner
manager: aolson
ms.date: 08/24/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mikefalkner
ms.search.validFrom: 2018-08-30
ms.dyn365.ops.version: 8.0.4
ms.openlocfilehash: 19e0528b95952de8e5503c361efcfeca4c529caf
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 01/29/2019
ms.locfileid: "359993"
---
# <a name="manage-international-bank-account-number-iban-validation"></a><span data-ttu-id="c96a7-103">إدارة التحقق من صحة رقم الحساب البنكي الدولي (IBAN)</span><span class="sxs-lookup"><span data-stu-id="c96a7-103">Manage International Bank Account Number (IBAN) validation</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="c96a7-104">تؤدي عملية التحقق من صحة رقم الحساب البنكي الدولي (IBAN) إلى زيادة مقدار عملية التحقق من الصحة التي يتم تنفيذها عند إضافة IBAN إلى حساب بنكي.</span><span class="sxs-lookup"><span data-stu-id="c96a7-104">International Bank Account Number (IBAN) validation increases the amount of validation that is done when you add an IBAN to a bank account.</span></span>

<span data-ttu-id="c96a7-105">يتم تخزين معلومات حول بنية IBAN في Microsoft Dynamics 365 for Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="c96a7-105">Information about the structure of the IBAN is stored in Microsoft Dynamics 365 for Finance and Operations.</span></span> <span data-ttu-id="c96a7-106">ويتم تحميل هذه المعلومات تلقائيًا عندما تستخدم IBAN للمرة الأولى على الحسابات البنكية.</span><span class="sxs-lookup"><span data-stu-id="c96a7-106">That information is automatically loaded when you first use the IBAN on bank accounts.</span></span> <span data-ttu-id="c96a7-107">تتضمن هذه المعلومات طول IBAN، ومواضع بدء رقم الحساب البنكي ورقم التوجيه البنكي وطول رقم الحساب البنكي ورقم التوجيه البنكي.</span><span class="sxs-lookup"><span data-stu-id="c96a7-107">It contains the length of the IBAN, the starting positions of the bank account number and the routing number, and the length of the bank account number and routing number.</span></span>

## <a name="set-up-iban-structures"></a><span data-ttu-id="c96a7-108">إعداد بنى IBAN‬</span><span class="sxs-lookup"><span data-stu-id="c96a7-108">Set up IBAN structures</span></span>

1. <span data-ttu-id="c96a7-109">انتقل إلى **إدارة النقد والبنك \> الإعداد \> بنى IBAN**.</span><span class="sxs-lookup"><span data-stu-id="c96a7-109">Go to **Cash and bank management \> Setup \> IBAN structures**.</span></span>
2. <span data-ttu-id="c96a7-110">لاحظ أن إعداد بنى IBAN لكل بلد أو منطقة قم تم بشكل تلقائي.</span><span class="sxs-lookup"><span data-stu-id="c96a7-110">Notice that the IBAN structures for each country or region have been set up automatically.</span></span>
3. <span data-ttu-id="c96a7-111">إذا أردت تخصيص البنى لبلد أو منطقة معينة، فيمكنك تحريرها.</span><span class="sxs-lookup"><span data-stu-id="c96a7-111">If you want to customize the structures for a specific country or region, you can edit them.</span></span>
4. <span data-ttu-id="c96a7-112">ستكون تعريفات البنية جزءًا من كل إصدار جديد.</span><span class="sxs-lookup"><span data-stu-id="c96a7-112">The structure definitions will be a part of each new release.</span></span> <span data-ttu-id="c96a7-113">يمكنك استخدام القائمة **إعادة تعيين البنى‬** لتحميل أحدث التعريفات بعد كل تحديث.</span><span class="sxs-lookup"><span data-stu-id="c96a7-113">You can use the **Reset structures** menu to load the latest definitions after each update.</span></span>

## <a name="validate-the-iban-structure-in-a-bank-account"></a><span data-ttu-id="c96a7-114">التحقق من صحة IBAN في بنية الحساب</span><span class="sxs-lookup"><span data-stu-id="c96a7-114">Validate the IBAN structure in a bank account</span></span>

1. <span data-ttu-id="c96a7-115">انتقل إلى **إدارة النقد والبنوك \> الحسابات البنكية \> الحسابات البنكية**.</span><span class="sxs-lookup"><span data-stu-id="c96a7-115">Go to **Cash and bank management \> Bank accounts \> Bank accounts**.</span></span>
2. <span data-ttu-id="c96a7-116">أنشئ حسابًا بنكيًا.</span><span class="sxs-lookup"><span data-stu-id="c96a7-116">Create a bank account.</span></span>
3. <span data-ttu-id="c96a7-117">على علامة التبويب السريعة **معلومات إضافية**، أدخل IBAN.</span><span class="sxs-lookup"><span data-stu-id="c96a7-117">On the **Additional information** FastTab, enter an IBAN.</span></span>

    <span data-ttu-id="c96a7-118">إذا لم يتطابق طول IBAN الطول المحدد لكل بلد أو منطقة، فستتلقى رسالة تحذير.</span><span class="sxs-lookup"><span data-stu-id="c96a7-118">If the length of the IBAN doesn't match the length that is defined for each country or region, you will receive a warning message.</span></span> <span data-ttu-id="c96a7-119">لا يمكنك المتابعة إذا لم يتطابق طول IBAN غير مع الطول المحدد في بنية IBAN.</span><span class="sxs-lookup"><span data-stu-id="c96a7-119">You can't continue if the length of the IBAN doesn't match the length specified in the IBAN structure.</span></span>

    <span data-ttu-id="c96a7-120">تتأكد أيضًا عملية من الصحة من أن رقم الحساب البنكي يتطابق مع جزء IBAN الذي يمثل رقم الحساب البنكي.</span><span class="sxs-lookup"><span data-stu-id="c96a7-120">The validation also verifies that the bank account number matches the part of the IBAN that represents the bank account number.</span></span> <span data-ttu-id="c96a7-121">إذا لم يكن رقم الحساب البنكي مطابقًا، فستتلقى رسالة تحذير.</span><span class="sxs-lookup"><span data-stu-id="c96a7-121">If the bank account number doesn't match, you will receive a warning message.</span></span> <span data-ttu-id="c96a7-122">هذه الرسالة عبارة عن تحذير فقط.</span><span class="sxs-lookup"><span data-stu-id="c96a7-122">This message is only a warning.</span></span> <span data-ttu-id="c96a7-123">يمكنك المتابعة حتى لو لم يكن رقم الحساب البنكي متطابقًا.</span><span class="sxs-lookup"><span data-stu-id="c96a7-123">You can continue even if the bank account number doesn't match.</span></span>

    <span data-ttu-id="c96a7-124">تتأكد أيضًا عملية من الصحة من أن رقم رقم التوجيه البنكي يتطابق مع جزء IBAN الذي يمثل رقم رقم التوجيه البنكي.</span><span class="sxs-lookup"><span data-stu-id="c96a7-124">The validation also verifies that the bank routing number matches the part of the IBAN that represents the bank routing number.</span></span> <span data-ttu-id="c96a7-125">يتضمن رقم التوجيه رقم بنك وفرع بنك إضافيًا في أغلب الأحيان.</span><span class="sxs-lookup"><span data-stu-id="c96a7-125">The routing number includes a bank number and often an additional bank branch.</span></span> <span data-ttu-id="c96a7-126">إذا لم يكن رقم التوجيه البنكي مطابقًا، فستتلقى رسالة تحذير.</span><span class="sxs-lookup"><span data-stu-id="c96a7-126">If the bank routing number doesn't match, you will receive a warning message.</span></span> <span data-ttu-id="c96a7-127">هذه الرسالة عبارة عن تحذير فقط.</span><span class="sxs-lookup"><span data-stu-id="c96a7-127">This message is only a warning.</span></span> <span data-ttu-id="c96a7-128">يمكنك المتابعة حتى لو لم يكن رقم التوجيه البنكي مطابقًا.</span><span class="sxs-lookup"><span data-stu-id="c96a7-128">You can continue even if the bank routing number doesn't match.</span></span>
