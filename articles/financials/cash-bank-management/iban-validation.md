---
title: "إدارة التحقق من صحة حساب رقم الحساب البنكي الدولي (IBAN)"
description: "يشرح هذا الموضوع كيفية إدارة التحقق من صحة حساب رقم الحساب البنكي الدولي (IBAN)."
author: mikefalkner
manager: aolson
ms.date: 08/24/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mikefalkner
ms.search.validFrom: 2018-08-30
ms.dyn365.ops.version: 8.0.4
ms.translationtype: HT
ms.sourcegitcommit: 98ed3378ab05c0c69c9e5b2a82310113a81c2264
ms.openlocfilehash: e091aab70a98e0f4b96c41c1ee48926947539105
ms.contentlocale: ar-sa
ms.lasthandoff: 08/31/2018

---

# <a name="manage-international-bank-account-number-iban-account-validation"></a><span data-ttu-id="8230c-103">إدارة التحقق من صحة حساب رقم الحساب البنكي الدولي (IBAN)</span><span class="sxs-lookup"><span data-stu-id="8230c-103">Manage International Bank Account Number (IBAN) account validation</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="8230c-104">تؤدي عملية التحقق من صحة حساب رقم الحساب البنكي الدولي (IBAN) إلى زيادة مقدار عملية التحقق من الصحة التي يتم تنفيذها عند إضافة IBAN إلى حساب بنكي.</span><span class="sxs-lookup"><span data-stu-id="8230c-104">International Bank Account Number (IBAN) account validation increases the amount of validation that is done when you add an IBAN to a bank account.</span></span>

<span data-ttu-id="8230c-105">يتم تخزين بنية IBAN في Microsoft Dynamics 365 for Finance and Operation، ويتم تحميلها تلقائيًا عندما تستخدم IBAN للمرة الأولى على الحسابات البنكية.</span><span class="sxs-lookup"><span data-stu-id="8230c-105">The structure of the IBAN is stored in Microsoft Dynamics 365 for Finance and Operation, and is automatically loaded when you first use the IBAN on bank accounts.</span></span> <span data-ttu-id="8230c-106">يعتبر رقم الحساب البنكي جزءًا من البنية المعرفة لرقم IBAN.</span><span class="sxs-lookup"><span data-stu-id="8230c-106">The bank account number is part of the structure defined for an IBAN number.</span></span> <span data-ttu-id="8230c-107">استنادًا إلى هذه البنية، إذا كان موضع وطول رقم الحساب في IBAN غير متطابق مع الموضع المحدد في البنية الخاصة بكل بلد أو منطقة، فستتلقى رسائل تحذير.</span><span class="sxs-lookup"><span data-stu-id="8230c-107">Based on that structure, if the position and length of the account number in the IBAN don't match the position that is defined in the structure for each country or region, you will receive warning messages.</span></span>

## <a name="set-up-iban-structures"></a><span data-ttu-id="8230c-108">إعداد بنى IBAN‬</span><span class="sxs-lookup"><span data-stu-id="8230c-108">Set up IBAN structures</span></span>

1. <span data-ttu-id="8230c-109">انتقل إلى **إدارة النقد والبنك \> الإعداد \> بنى IBAN**.</span><span class="sxs-lookup"><span data-stu-id="8230c-109">Go to **Cash and bank management \> Setup \> IBAN structures**.</span></span>
2. <span data-ttu-id="8230c-110">لاحظ أن إعداد بنى IBAN لكل بلد أو منطقة قم تم بشكل تلقائي.</span><span class="sxs-lookup"><span data-stu-id="8230c-110">Notice that the IBAN structures for each country or region have been set up automatically.</span></span>
3. <span data-ttu-id="8230c-111">إذا كان يجب تخصيص البنى لبلد أو منطقة معينة، فيمكنك تحريرها.</span><span class="sxs-lookup"><span data-stu-id="8230c-111">If you must customize the structures for a specific country or region, you can edit them.</span></span>
4. <span data-ttu-id="8230c-112">ستكون تعريفات البنية جزءًا من كل إصدار جديد.</span><span class="sxs-lookup"><span data-stu-id="8230c-112">The structure definitions will be a part of each new release.</span></span> <span data-ttu-id="8230c-113">يمكنك استخدام القائمة **إعادة تعيين البنى‬** لتحميل أحدث التعريفات بعد كل تحديث.</span><span class="sxs-lookup"><span data-stu-id="8230c-113">You can use the **Reset structures** menu to load the latest definitions after each update.</span></span>

## <a name="validate-the-iban-structure-in-a-bank-account"></a><span data-ttu-id="8230c-114">التحقق من صحة IBAN في بنية الحساب</span><span class="sxs-lookup"><span data-stu-id="8230c-114">Validate the IBAN structure in a bank account</span></span>

1. <span data-ttu-id="8230c-115">انتقل إلى **إدارة النقد والبنوك \> الحسابات البنكية \> الحسابات البنكية**.</span><span class="sxs-lookup"><span data-stu-id="8230c-115">Go to **Cash and bank management \> Bank accounts \> Bank accounts**.</span></span>
2. <span data-ttu-id="8230c-116">أنشئ حسابًا بنكيًا.</span><span class="sxs-lookup"><span data-stu-id="8230c-116">Create a bank account.</span></span>
3. <span data-ttu-id="8230c-117">على علامة التبويب السريعة **معلومات إضافية**، أدخل IBAN.</span><span class="sxs-lookup"><span data-stu-id="8230c-117">On the **Additional information** FastTab, enter an IBAN.</span></span>

    <span data-ttu-id="8230c-118">إذا كان موضع وطول رقم الحساب في IBAN غير متطابق مع الموضع المحدد في البنية الخاصة بكل بلد أو منطقة، فستتلقى رسالة تحذير.</span><span class="sxs-lookup"><span data-stu-id="8230c-118">If the position and length of the account number in the IBAN don't match the position that is defined in the structure for each country or region, you receive a message.</span></span> <span data-ttu-id="8230c-119">لا يمكنك المتابعة إذا كان طول IBAN غير متوافق مع الطول في بنية IBAN.</span><span class="sxs-lookup"><span data-stu-id="8230c-119">You can't continue if the length of the IBAN doesn't match the length in the IBAN structure.</span></span>

    <span data-ttu-id="8230c-120">تتأكد أيضًا عملية من الصحة من أن رقم الحساب البنكي يتطابق مع جزء IBAN الذي يمثل رقم الحساب البنكي.</span><span class="sxs-lookup"><span data-stu-id="8230c-120">The validation also verifies that the bank account number matches the part of the IBAN that represents the bank account number.</span></span> <span data-ttu-id="8230c-121">إذا لم يكن رقم الحساب البنكي مطابقًا، تتلقى رسالة تحذير.</span><span class="sxs-lookup"><span data-stu-id="8230c-121">If the bank account number doesn't match, you receive a warning message.</span></span> <span data-ttu-id="8230c-122">هذه الرسالة عبارة عن تحذير فقط.</span><span class="sxs-lookup"><span data-stu-id="8230c-122">This message is only a warning.</span></span> <span data-ttu-id="8230c-123">يمكنك المتابعة حتى لو لم يكن رقم الحساب البنكي متطابقًا.</span><span class="sxs-lookup"><span data-stu-id="8230c-123">You can continue even if the bank account number doesn't match.</span></span>

