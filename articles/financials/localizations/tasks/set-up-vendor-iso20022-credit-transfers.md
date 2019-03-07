---
title: إعداد المورّدين والحسابات البنكية للمورّدين لتحويلات الائتمان ISO20022
description: يوضح هذا الإجراء كيفية إعداد المورّد والمعلومات المحددة الخاصة بالحساب البنكي للمورّد والمطلوبة لتحويل الائتمان ISO20022 أو أي عملية أخرى لإنشاء ملف دفع المورّد.
author: mrolecki
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: VendTable, VendBankAccounts
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mrolecki
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 13b3c37f5d013dd896a456018813f20e5e70350b
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 01/29/2019
ms.locfileid: "311601"
---
# <a name="set-up-vendors-and-vendor-bank-accounts-for-iso20022-credit-transfers"></a><span data-ttu-id="74360-103">إعداد المورّدين والحسابات البنكية للمورّدين لتحويلات الائتمان ISO20022</span><span class="sxs-lookup"><span data-stu-id="74360-103">Set up vendors and vendor bank accounts for ISO20022 credit transfers</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="74360-104">يوضح هذا الإجراء كيفية إعداد المورّد والمعلومات المحددة الخاصة بالحساب البنكي للمورّد والمطلوبة لتحويل الائتمان ISO20022 أو أي عملية أخرى لإنشاء ملف دفع المورّد.</span><span class="sxs-lookup"><span data-stu-id="74360-104">This procedure demonstrates how to set up the vendor and vendor specific bank account information required for ISO20022 Credit transfer or any other vendor payment file generation.</span></span> 

<span data-ttu-id="74360-105">شركة بيانات العرض التوضيحي التي تم استخدامها لإنشاء هذا الإجراء هي DEMF.</span><span class="sxs-lookup"><span data-stu-id="74360-105">The demo data company used to create this procedure is DEMF.</span></span>
<span data-ttu-id="74360-106">هذا هو الإجراء الرابع من ضمن الإجراءات الخمسة، هدفه توضيح عملية معالجة مدفوعات المورّد باستخدام تكوينات التقارير الإلكترونية.</span><span class="sxs-lookup"><span data-stu-id="74360-106">This is the fourth procedure, out of five, that illustrates the vendor payment process using electronic reporting configurations.</span></span> <span data-ttu-id="74360-107">يتم استخدام هذا الإجراء لميزة تمت إضافتها في Dynamics 365 for Operations، الإصدار 1611.</span><span class="sxs-lookup"><span data-stu-id="74360-107">This procedure is for a feature that was added in Dynamics 365 for Operations version 1611.</span></span>


## <a name="set-up-bank-details"></a><span data-ttu-id="74360-108">إعداد تفاصيل البنك</span><span class="sxs-lookup"><span data-stu-id="74360-108">Set up bank details</span></span>
1. <span data-ttu-id="74360-109">انتقل إلى الحسابات الدائنة > الموردون > كافة الموردين.</span><span class="sxs-lookup"><span data-stu-id="74360-109">Go to Accounts payable > Vendors > All vendors.</span></span>
2. <span data-ttu-id="74360-110">استخدم عامل التصفية السريع للبحث عن السجلات.</span><span class="sxs-lookup"><span data-stu-id="74360-110">Use the Quick Filter to find records.</span></span> <span data-ttu-id="74360-111">على سبيل المثال، قم بإجراء التصفية على حقل "حساب المورّد" بقيمة "DE-001".</span><span class="sxs-lookup"><span data-stu-id="74360-111">For example, filter on the Vendor account field with a value of 'DE-001'.</span></span>
3. <span data-ttu-id="74360-112">انقر فوق DE-001 لفتح تفاصيل المورّد.</span><span class="sxs-lookup"><span data-stu-id="74360-112">Click DE-001 to open vendor details.</span></span>
4. <span data-ttu-id="74360-113">في جزء الإجراءات، انقر فوق "المورّد".</span><span class="sxs-lookup"><span data-stu-id="74360-113">On the Action Pane, click Vendor.</span></span>
5. <span data-ttu-id="74360-114">انتقل إلى "الحسابات البنكية".</span><span class="sxs-lookup"><span data-stu-id="74360-114">Click Bank accounts.</span></span>
6. <span data-ttu-id="74360-115">انقر فوق "تحرير".</span><span class="sxs-lookup"><span data-stu-id="74360-115">Click Edit.</span></span>
    * <span data-ttu-id="74360-116">إذا لم يتوفر أي حساب بنكي، فتحتاج إلى إنشاء واحد جديد.</span><span class="sxs-lookup"><span data-stu-id="74360-116">If there is no bank account available, you need to create a new one.</span></span>  
7. <span data-ttu-id="74360-117">في الحقل "كود التحويل الإلكتروني‬"، اكتب "COBADEFFXXX".</span><span class="sxs-lookup"><span data-stu-id="74360-117">In the SWIFT code field, type 'COBADEFFXXX'.</span></span>
8. <span data-ttu-id="74360-118">في الحقل "IBAN"، اكتب ''DE36200400000628808808".</span><span class="sxs-lookup"><span data-stu-id="74360-118">In the IBAN field, type 'DE36200400000628808808'.</span></span>
9. <span data-ttu-id="74360-119">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="74360-119">Close the page.</span></span>

## <a name="set-up-a-method-of-payment-for-the-vendor"></a><span data-ttu-id="74360-120">إعداد طريقة دفع للمورّد</span><span class="sxs-lookup"><span data-stu-id="74360-120">Set up a method of payment for the vendor</span></span>
1. <span data-ttu-id="74360-121">انقر فوق "تحرير".</span><span class="sxs-lookup"><span data-stu-id="74360-121">Click Edit.</span></span>
2. <span data-ttu-id="74360-122">قم بتوسيع أو طي قسم الدفع.</span><span class="sxs-lookup"><span data-stu-id="74360-122">Expand or collapse the Payment section.</span></span>
3. <span data-ttu-id="74360-123">في الحقل "طريقة الدفع"، انقر فوق زر القائمة المنسدلة لفتح البحث.</span><span class="sxs-lookup"><span data-stu-id="74360-123">In the Method of payment field, click the drop-down button to open the lookup.</span></span>
4. <span data-ttu-id="74360-124">في القائمة، انقر فوق الارتباط في الصف سيبا CT.</span><span class="sxs-lookup"><span data-stu-id="74360-124">In the list, click the link in the SEPA CT row.</span></span>
5. <span data-ttu-id="74360-125">انقر فوق "حفظ".</span><span class="sxs-lookup"><span data-stu-id="74360-125">Click Save.</span></span>

