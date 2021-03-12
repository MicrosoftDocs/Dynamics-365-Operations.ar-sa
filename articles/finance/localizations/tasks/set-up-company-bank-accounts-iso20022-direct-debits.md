---
title: إعداد الحسابات البنكية للشركة للديون المباشرة ISO20022
description: تنقلك هذه المهمة عبر عملية إعداد المعلومات المحددة الخاصة بالحساب البنكي للشركة والمطلوبة لإنشاء ملفات دفع العميل.
author: mrolecki
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: BankAccountTable, OMLegalEntity, BankAccountTableLookUp
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: mrolecki
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: b0faa23193111ed771ccc3a5c7f99ca908a036e9
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 01/15/2021
ms.locfileid: "4988126"
---
# <a name="set-up-company-bank-accounts-for-iso20022-direct-debits"></a><span data-ttu-id="4bcc7-103">إعداد الحسابات البنكية للشركة للديون المباشرة ISO20022</span><span class="sxs-lookup"><span data-stu-id="4bcc7-103">Set up company bank accounts for ISO20022 direct debits</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="4bcc7-104">تنقلك هذه المهمة عبر عملية إعداد المعلومات المحددة الخاصة بالحساب البنكي للشركة والمطلوبة لإنشاء ملفات دفع العميل.</span><span class="sxs-lookup"><span data-stu-id="4bcc7-104">This task walks you through setting up the company specific bank account information that is required for generating customer payment files.</span></span> <span data-ttu-id="4bcc7-105">يستخدم هذا الإجراء تنسيق الدين المباشر ISO 20022 كمثال.</span><span class="sxs-lookup"><span data-stu-id="4bcc7-105">This procedure uses the ISO 20022 direct debit format as an example.</span></span> <span data-ttu-id="4bcc7-106">قد تتطلب تنسيقات أخرى معلومات إعداد إضافية، مثل "معرف الشركة" أو "كود الفرز".</span><span class="sxs-lookup"><span data-stu-id="4bcc7-106">Other formats might require additional setup information like the Company ID or the Sort code.</span></span>



<span data-ttu-id="4bcc7-107">تم إنشاء هذه المهمة باستخدام شركة بيانات العرض التوضيحي DEMF.</span><span class="sxs-lookup"><span data-stu-id="4bcc7-107">This task was created using the demo data company DEMF.</span></span>



<span data-ttu-id="4bcc7-108">هذا هو الإجراء الثاني من ضمن خمسة إجراءات هدفها توضيح عملية معالجة مدفوعات العميل باستخدام تكوينات التقارير الإلكترونية.</span><span class="sxs-lookup"><span data-stu-id="4bcc7-108">This is the second of five procedures that demonstrate the customer payment process using electronic reporting configurations.</span></span>


## <a name="set-up-the-iban-and-swift-codes"></a><span data-ttu-id="4bcc7-109">إعداد أكواد IBAN والتحويل الإلكتروني‬</span><span class="sxs-lookup"><span data-stu-id="4bcc7-109">Set up the IBAN and SWIFT codes</span></span>
1. <span data-ttu-id="4bcc7-110">انتقل إلى إدارة النقد والبنوك > الحسابات البنكية.</span><span class="sxs-lookup"><span data-stu-id="4bcc7-110">Go to Cash and bank management > Bank accounts.</span></span>
2. <span data-ttu-id="4bcc7-111">استخدم عامل التصفية السريع لإجراء التصفية على الحقل "الحساب البنكي‬" بالقيمة "DEMF OPER''.</span><span class="sxs-lookup"><span data-stu-id="4bcc7-111">Use the Quick Filter to filter on the Bank account field with a value of 'DEMF OPER'.</span></span>
3. <span data-ttu-id="4bcc7-112">في القائمة، انقر فوق الارتباط في الصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="4bcc7-112">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="4bcc7-113">على سبيل المثال، انقر فوق 'DEMF OPER' لفتح تفاصيل الحساب البنكي.</span><span class="sxs-lookup"><span data-stu-id="4bcc7-113">For example, click 'DEMF OPER' to open the bank account details.</span></span>  
4. <span data-ttu-id="4bcc7-114">انقر فوق "تحرير".</span><span class="sxs-lookup"><span data-stu-id="4bcc7-114">Click Edit.</span></span>
5. <span data-ttu-id="4bcc7-115">‏‫قم بتوسيع المقطع "تعريف إضافي" أو طيّه.</span><span class="sxs-lookup"><span data-stu-id="4bcc7-115">Expand or collapse the Additional identification section.</span></span>
6. <span data-ttu-id="4bcc7-116">في الحقل "IBAN‬"، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="4bcc7-116">In the IBAN field, type a value.</span></span>
    * <span data-ttu-id="4bcc7-117">على سبيل المثال، أدخل "DE89370400440532013000".</span><span class="sxs-lookup"><span data-stu-id="4bcc7-117">For example, enter 'DE89370400440532013000'.</span></span>  
7. <span data-ttu-id="4bcc7-118">في الحقل "كود التحويل الإلكتروني‬"، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="4bcc7-118">In the SWIFT code field, type a value.</span></span>
    * <span data-ttu-id="4bcc7-119">على سبيل المثال، أدخل "DEUTDEFF".</span><span class="sxs-lookup"><span data-stu-id="4bcc7-119">For example, enter 'DEUTDEFF'.</span></span>    <span data-ttu-id="4bcc7-120">لاحظ أن SWIFT \ BIC غير إلزامي للعديد من تنسيقات الدفع، لكن من المستحسن أن يتم تسجيله لحساب بنكي.</span><span class="sxs-lookup"><span data-stu-id="4bcc7-120">Please note that SWIFT \ BIC is not mandatory for many payment formats however it is recommended to have it registered for a bank account.</span></span>  
8. <span data-ttu-id="4bcc7-121">انقر فوق "حفظ".</span><span class="sxs-lookup"><span data-stu-id="4bcc7-121">Click Save.</span></span>

## <a name="set-up-a-bank-account-for-the-legal-entity"></a><span data-ttu-id="4bcc7-122">إعداد حساب بنكي للكيان القانوني</span><span class="sxs-lookup"><span data-stu-id="4bcc7-122">Set up a bank account for the legal entity</span></span>
1. <span data-ttu-id="4bcc7-123">انتقل إلى إدارة المؤسسة > المؤسسات > الكيانات القانونية.</span><span class="sxs-lookup"><span data-stu-id="4bcc7-123">Go to Organization administration > Organizations > Legal entities.</span></span>
2. <span data-ttu-id="4bcc7-124">انقر فوق "تحرير".</span><span class="sxs-lookup"><span data-stu-id="4bcc7-124">Click Edit.</span></span>
3. <span data-ttu-id="4bcc7-125">‏‫قم بتوسيع المقطع "معلومات الحساب البنكي‬" أو طيّه.</span><span class="sxs-lookup"><span data-stu-id="4bcc7-125">Expand or collapse the Bank account information section.</span></span>
4. <span data-ttu-id="4bcc7-126">في الحقل "الحساب البنكي"، انقر فوق زر القائمة المنسدلة لفتح البحث.</span><span class="sxs-lookup"><span data-stu-id="4bcc7-126">In the Bank account field, click the drop-down button to open the lookup.</span></span>
5. <span data-ttu-id="4bcc7-127">في القائمة، انقر فوق الارتباط في الصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="4bcc7-127">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="4bcc7-128">على سبيل المثال، حدد الحساب البنكي "DEMF OPER".</span><span class="sxs-lookup"><span data-stu-id="4bcc7-128">For example, select the "DEMF OPER" bank account.</span></span>  
6. <span data-ttu-id="4bcc7-129">انقر فوق "حفظ".</span><span class="sxs-lookup"><span data-stu-id="4bcc7-129">Click Save.</span></span>

