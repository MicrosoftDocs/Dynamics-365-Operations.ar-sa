---
title: إعداد الحسابات البنكية للشركة لتحويلات الائتمان ISO20022
description: يوضح هذا الإجراء كيفية إعداد المعلومات المحددة الخاصة بالحساب البنكي للشركة والمطلوبة لإنشاء ملف الدفع.
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
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mrolecki
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 2bbbf55ed28ad2131d7e1253dd44842d85d39315
ms.sourcegitcommit: 16bfa0fd08feec1647829630401ce62ce2ffa1a4
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 08/02/2019
ms.locfileid: "1848734"
---
# <a name="set-up-company-bank-accounts-for-iso20022-credit-transfers"></a><span data-ttu-id="38239-103">إعداد الحسابات البنكية للشركة لتحويلات الائتمان ISO20022</span><span class="sxs-lookup"><span data-stu-id="38239-103">Set up company bank accounts for ISO20022 credit transfers</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="38239-104">يوضح هذا الإجراء كيفية إعداد المعلومات المحددة الخاصة بالحساب البنكي للشركة والمطلوبة لإنشاء ملف الدفع.</span><span class="sxs-lookup"><span data-stu-id="38239-104">This procedure shows how to set up company-specific bank account information that is required for payment file generation.</span></span> <span data-ttu-id="38239-105">يمكنك إعداد المعلومات المطلوبة لإنشاء تنسيق تحويل الائتمان 20022 ISO، ولكن استنادًا إلى التنسيق قد تكون هناك معلومات أخرى مطلوبة، مثل "معرف الشركة" أو "كود الفرز".</span><span class="sxs-lookup"><span data-stu-id="38239-105">You set up information required to generate ISO 20022 credit transfer format but depending on the format there might be other information required, such as the Company ID or the Sort code.</span></span> 

<span data-ttu-id="38239-106">شركة بيانات العرض التوضيحي التي تم استخدامها لإنشاء هذا الإجراء هي DEMF.</span><span class="sxs-lookup"><span data-stu-id="38239-106">The demo data company used to create this procedure is DEMF.</span></span>

<span data-ttu-id="38239-107">هذه هو الإجراء الثاني من ضمن الإجراءات الخمسة، هدفه توضيح عملية معالجة مدفوعات المورّد باستخدام تكوينات التقارير الإلكترونية.</span><span class="sxs-lookup"><span data-stu-id="38239-107">This is the second procedure, out of five, that illustrates the vendor payment process using electronic reporting configurations.</span></span> <span data-ttu-id="38239-108">يتم استخدام هذا الإجراء لميزة تمت إضافتها في Dynamics 365 for Operations، الإصدار 1611.</span><span class="sxs-lookup"><span data-stu-id="38239-108">This procedure is for a feature that was added in Dynamics 365 for Operations version 1611.</span></span>


## <a name="set-up-iban-and-swift-code"></a><span data-ttu-id="38239-109">إعداد كود IBAN وكود التحويل الإلكتروني</span><span class="sxs-lookup"><span data-stu-id="38239-109">Set up IBAN and SWIFT code</span></span>
1. <span data-ttu-id="38239-110">انتقل إلى إدارة النقد والبنوك > الحسابات البنكية.</span><span class="sxs-lookup"><span data-stu-id="38239-110">Go to Cash and bank management > Bank accounts.</span></span>
2. <span data-ttu-id="38239-111">استخدم عامل التصفية السريع لإجراء التصفية على الحقل "الحساب البنكي‬" بالقيمة "DEMF OPER''.</span><span class="sxs-lookup"><span data-stu-id="38239-111">Use the Quick Filter to filter on the Bank account field with a value of 'DEMF OPER'.</span></span>
3. <span data-ttu-id="38239-112">انقر فوق "DEMF OPER" لفتح تفاصيل الحساب البنكي.</span><span class="sxs-lookup"><span data-stu-id="38239-112">Click DEMF OPER to open bank account details.</span></span>
4. <span data-ttu-id="38239-113">انقر فوق "تحرير".</span><span class="sxs-lookup"><span data-stu-id="38239-113">Click Edit.</span></span>
5. <span data-ttu-id="38239-114">‏‫قم بتوسيع المقطع "تعريف إضافي".</span><span class="sxs-lookup"><span data-stu-id="38239-114">Expand the Additional identification section.</span></span>
6. <span data-ttu-id="38239-115">في الحقل "IBAN"، اكتب ''DE89370400440532013000".</span><span class="sxs-lookup"><span data-stu-id="38239-115">In the IBAN field, type 'DE89370400440532013000'.</span></span>
7. <span data-ttu-id="38239-116">في الحقل "كود التحويل الإلكتروني‬"، اكتب "DEUTDEFF".</span><span class="sxs-lookup"><span data-stu-id="38239-116">In the SWIFT code field, type 'DEUTDEFF'.</span></span>
    * <span data-ttu-id="38239-117">لاحظ أن SWIFT\BIC غير مطلوب للعديد من تنسيقات الدفع، لكن من المستحسن أن يتم تسجيله لحساب بنكي.</span><span class="sxs-lookup"><span data-stu-id="38239-117">Note that SWIFT\BIC is not required for many payment formats, however it is recommended to have it registered for a bank account.</span></span>  
8. <span data-ttu-id="38239-118">انقر فوق "حفظ".</span><span class="sxs-lookup"><span data-stu-id="38239-118">Click Save.</span></span>

## <a name="set-up-bank-account-for-the-legal-entity"></a><span data-ttu-id="38239-119">إعداد الحساب البنكي للكيان القانوني</span><span class="sxs-lookup"><span data-stu-id="38239-119">Set up bank account for the legal entity</span></span>
1. <span data-ttu-id="38239-120">انتقل إلى إدارة المؤسسة > المؤسسات > الكيانات القانونية.</span><span class="sxs-lookup"><span data-stu-id="38239-120">Go to Organization administration > Organizations > Legal entities.</span></span>
2. <span data-ttu-id="38239-121">انقر فوق "تحرير".</span><span class="sxs-lookup"><span data-stu-id="38239-121">Click Edit.</span></span>
3. <span data-ttu-id="38239-122">‏‫قم بتوسيع القسم "معلومات الحساب البنكي‬".</span><span class="sxs-lookup"><span data-stu-id="38239-122">Expand the Bank account information section.</span></span>
4. <span data-ttu-id="38239-123">في الحقل "الحساب البنكي‬‬"، أدخل قيمة أو حددها.</span><span class="sxs-lookup"><span data-stu-id="38239-123">In the Bank account field, enter or select a value.</span></span>
5. <span data-ttu-id="38239-124">انقر فوق "حفظ".</span><span class="sxs-lookup"><span data-stu-id="38239-124">Click Save.</span></span>

