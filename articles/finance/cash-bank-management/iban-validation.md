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
ms.reviewer: roschlom
ms.search.region: Global
ms.author: roschlom
ms.search.validFrom: 2018-08-30
ms.dyn365.ops.version: 8.0.4
ms.openlocfilehash: f3e7376827a42034e68cb0ee492b82f7274930ea
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 02/15/2021
ms.locfileid: "5253977"
---
# <a name="manage-international-bank-account-number-iban-account-validation"></a><span data-ttu-id="18f69-103">إدارة التحقق من صحة حساب رقم الحساب البنكي الدولي (IBAN)</span><span class="sxs-lookup"><span data-stu-id="18f69-103">Manage International Bank Account Number (IBAN) account validation</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="18f69-104">تؤدي عملية التحقق من صحة رقم الحساب البنكي الدولي (IBAN) إلى زيادة مقدار عملية التحقق من الصحة التي يتم تنفيذها عند إضافة IBAN إلى حساب بنكي.</span><span class="sxs-lookup"><span data-stu-id="18f69-104">International Bank Account Number (IBAN) validation increases the amount of validation that is done when you add an IBAN to a bank account.</span></span>

<span data-ttu-id="18f69-105">يتم تخزين معلومات حول بنية IBAN في Microsoft Dynamics 365 Finance.</span><span class="sxs-lookup"><span data-stu-id="18f69-105">Information about the structure of the IBAN is stored in Microsoft Dynamics 365 Finance.</span></span> <span data-ttu-id="18f69-106">ويتم تحميل هذه المعلومات تلقائيًا عندما تستخدم IBAN للمرة الأولى على الحسابات البنكية.</span><span class="sxs-lookup"><span data-stu-id="18f69-106">That information is automatically loaded when you first use the IBAN on bank accounts.</span></span> <span data-ttu-id="18f69-107">تتضمن هذه المعلومات طول IBAN، ومواضع بدء رقم الحساب البنكي ورقم التوجيه البنكي وطول رقم الحساب البنكي ورقم التوجيه البنكي.</span><span class="sxs-lookup"><span data-stu-id="18f69-107">It contains the length of the IBAN, the starting positions of the bank account number and the routing number, and the length of the bank account number and routing number.</span></span>

## <a name="set-up-iban-structures"></a><span data-ttu-id="18f69-108">إعداد بنى IBAN‬</span><span class="sxs-lookup"><span data-stu-id="18f69-108">Set up IBAN structures</span></span>

1. <span data-ttu-id="18f69-109">انتقل إلى **إدارة النقد والبنك \> الإعداد \> بنى IBAN**.</span><span class="sxs-lookup"><span data-stu-id="18f69-109">Go to **Cash and bank management \> Setup \> IBAN structures**.</span></span>
2. <span data-ttu-id="18f69-110">لاحظ أن إعداد بنى IBAN لكل بلد أو منطقة قم تم بشكل تلقائي.</span><span class="sxs-lookup"><span data-stu-id="18f69-110">Notice that the IBAN structures for each country or region have been set up automatically.</span></span>
3. <span data-ttu-id="18f69-111">إذا أردت تخصيص البنى لبلد أو منطقة معينة، فيمكنك تحريرها.</span><span class="sxs-lookup"><span data-stu-id="18f69-111">If you want to customize the structures for a specific country or region, you can edit them.</span></span>
4. <span data-ttu-id="18f69-112">ستكون تعريفات البنية جزءًا من كل إصدار جديد.</span><span class="sxs-lookup"><span data-stu-id="18f69-112">The structure definitions will be a part of each new release.</span></span> <span data-ttu-id="18f69-113">يمكنك استخدام القائمة **إعادة تعيين البنى‬** لتحميل أحدث التعريفات بعد كل تحديث.</span><span class="sxs-lookup"><span data-stu-id="18f69-113">You can use the **Reset structures** menu to load the latest definitions after each update.</span></span>

## <a name="validate-the-iban-structure-in-a-bank-account"></a><span data-ttu-id="18f69-114">التحقق من صحة IBAN في بنية الحساب</span><span class="sxs-lookup"><span data-stu-id="18f69-114">Validate the IBAN structure in a bank account</span></span>

1. <span data-ttu-id="18f69-115">انتقل إلى **إدارة النقد والبنوك \> الحسابات البنكية \> الحسابات البنكية**.</span><span class="sxs-lookup"><span data-stu-id="18f69-115">Go to **Cash and bank management \> Bank accounts \> Bank accounts**.</span></span>
2. <span data-ttu-id="18f69-116">أنشئ حسابًا بنكيًا.</span><span class="sxs-lookup"><span data-stu-id="18f69-116">Create a bank account.</span></span>
3. <span data-ttu-id="18f69-117">على علامة التبويب السريعة **معلومات إضافية**، أدخل IBAN.</span><span class="sxs-lookup"><span data-stu-id="18f69-117">On the **Additional information** FastTab, enter an IBAN.</span></span>

    <span data-ttu-id="18f69-118">إذا لم يتطابق طول IBAN الطول المحدد لكل بلد أو منطقة، فستتلقى رسالة تحذير.</span><span class="sxs-lookup"><span data-stu-id="18f69-118">If the length of the IBAN doesn't match the length that is defined for each country or region, you will receive a warning message.</span></span> <span data-ttu-id="18f69-119">لا يمكنك المتابعة إذا لم يتطابق طول IBAN غير مع الطول المحدد في بنية IBAN.</span><span class="sxs-lookup"><span data-stu-id="18f69-119">You can't continue if the length of the IBAN doesn't match the length specified in the IBAN structure.</span></span>

    <span data-ttu-id="18f69-120">تتأكد أيضًا عملية من الصحة من أن رقم الحساب البنكي يتطابق مع جزء IBAN الذي يمثل رقم الحساب البنكي.</span><span class="sxs-lookup"><span data-stu-id="18f69-120">The validation also verifies that the bank account number matches the part of the IBAN that represents the bank account number.</span></span> <span data-ttu-id="18f69-121">إذا لم يكن رقم الحساب البنكي مطابقًا، فستتلقى رسالة تحذير.</span><span class="sxs-lookup"><span data-stu-id="18f69-121">If the bank account number doesn't match, you will receive a warning message.</span></span> <span data-ttu-id="18f69-122">هذه الرسالة عبارة عن تحذير فقط.</span><span class="sxs-lookup"><span data-stu-id="18f69-122">This message is only a warning.</span></span> <span data-ttu-id="18f69-123">يمكنك المتابعة حتى لو لم يكن رقم الحساب البنكي متطابقًا.</span><span class="sxs-lookup"><span data-stu-id="18f69-123">You can continue even if the bank account number doesn't match.</span></span>

    <span data-ttu-id="18f69-124">تتأكد أيضًا عملية من الصحة من أن رقم رقم التوجيه البنكي يتطابق مع جزء IBAN الذي يمثل رقم رقم التوجيه البنكي.</span><span class="sxs-lookup"><span data-stu-id="18f69-124">The validation also verifies that the bank routing number matches the part of the IBAN that represents the bank routing number.</span></span> <span data-ttu-id="18f69-125">يتضمن رقم التوجيه رقم بنك وفرع بنك إضافيًا في أغلب الأحيان.</span><span class="sxs-lookup"><span data-stu-id="18f69-125">The routing number includes a bank number and often an additional bank branch.</span></span> <span data-ttu-id="18f69-126">إذا لم يكن رقم التوجيه البنكي مطابقًا، فستتلقى رسالة تحذير.</span><span class="sxs-lookup"><span data-stu-id="18f69-126">If the bank routing number doesn't match, you will receive a warning message.</span></span> <span data-ttu-id="18f69-127">هذه الرسالة عبارة عن تحذير فقط.</span><span class="sxs-lookup"><span data-stu-id="18f69-127">This message is only a warning.</span></span> <span data-ttu-id="18f69-128">يمكنك المتابعة حتى لو لم يكن رقم التوجيه البنكي مطابقًا.</span><span class="sxs-lookup"><span data-stu-id="18f69-128">You can continue even if the bank routing number doesn't match.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]