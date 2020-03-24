---
title: إنشاء أمر شراء لمورد مرة واحدة
description: يوضح هذا الإجراء كيفية إنشاء أمر شراء لمورّد لمرة واحدة.
author: FrankDahl
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: PurchTable, PurchCreateOrder
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: fdahl
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: e2fa54ff598bb6a09bbcc483995a6e1a3f4286b3
ms.sourcegitcommit: 16612a632aad9d390f8d80d3fc1f766585b2911e
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 03/04/2020
ms.locfileid: "3098066"
---
# <a name="create-a-purchase-order-for-a-one-time-supplier"></a><span data-ttu-id="dde9f-103">إنشاء أمر شراء لمورد مرة واحدة</span><span class="sxs-lookup"><span data-stu-id="dde9f-103">Create a purchase order for a one-time supplier</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="dde9f-104">يوضح هذا الإجراء كيفية إنشاء أمر شراء لمورّد لمرة واحدة.</span><span class="sxs-lookup"><span data-stu-id="dde9f-104">This procedure shows you how to create a purchase order for a one-time supplier.</span></span> <span data-ttu-id="dde9f-105">يتم إنشاء المورّد مع أمر الشراء بشكل تلقائي، بدلاً من إنشاء حساب المورّد يدويًا.</span><span class="sxs-lookup"><span data-stu-id="dde9f-105">The supplier is created automatically with the purchase order, rather than having to create the vendor account manually.</span></span> <span data-ttu-id="dde9f-106">وعادة ما يتم إنشاء أوامر الشراء عن طريق وكيل شراء.</span><span class="sxs-lookup"><span data-stu-id="dde9f-106">Purchase orders are typically created by a purchasing agent.</span></span> <span data-ttu-id="dde9f-107">يمكن استخدام المثال المعروض في هذا الدليل في شركة بيانات العرض التوضيحي USMF.</span><span class="sxs-lookup"><span data-stu-id="dde9f-107">The example shown in this guide can be used in the USMF demo data company.</span></span> <span data-ttu-id="dde9f-108">يجب إعداد حساب مورّد لمرة واحدة في صفحة "محددات الحسابات الدائنة".</span><span class="sxs-lookup"><span data-stu-id="dde9f-108">It is a prerequisite that a one-time vendor account has been set up in the Account payable parameters page.</span></span>


## <a name="create-a-purchase-order-for-a-one-time-supplier"></a><span data-ttu-id="dde9f-109">إنشاء أمر شراء لمورد مرة واحدة</span><span class="sxs-lookup"><span data-stu-id="dde9f-109">Create a purchase order for a one-time supplier</span></span>
1. <span data-ttu-id="dde9f-110">انتقل إلى التدبير وتحديد الموارد > أوامر الشراء > كل أوامر الشراء.</span><span class="sxs-lookup"><span data-stu-id="dde9f-110">Go to Procurement and sourcing > Purchase orders > All purchase orders.</span></span>
2. <span data-ttu-id="dde9f-111">انقر فوق "جديد".</span><span class="sxs-lookup"><span data-stu-id="dde9f-111">Click New.</span></span>
3. <span data-ttu-id="dde9f-112">حدد "نعم" في الحقل "مورد مرة واحدة‬".</span><span class="sxs-lookup"><span data-stu-id="dde9f-112">Select Yes in the One-time supplier field.</span></span>
    * <span data-ttu-id="dde9f-113">يتم إنشاء حساب مورّد وتعيينه إلى أمر الشراء تلقائيًا.</span><span class="sxs-lookup"><span data-stu-id="dde9f-113">A vendor account is automatically created and assigned to the purchase order.</span></span> <span data-ttu-id="dde9f-114">يتم إنشاء حساب المورّد استنادًا إلى القالب المحدد في علامة التبويب "عام" في صفحة "محددات الحسابات الدائنة‬".</span><span class="sxs-lookup"><span data-stu-id="dde9f-114">The vendor account is created based on the template that is specified on the General tab in the Accounts payable parameters page.</span></span>  
4. <span data-ttu-id="dde9f-115">في حقل "الاسم"، اكتب اسمًا للمورّد.</span><span class="sxs-lookup"><span data-stu-id="dde9f-115">In the Name field, type a name for the supplier.</span></span>
5. <span data-ttu-id="dde9f-116">انقر فوق "موافق".</span><span class="sxs-lookup"><span data-stu-id="dde9f-116">Click OK.</span></span>
    * <span data-ttu-id="dde9f-117">يمكنك الآن إكمال أمر الشراء ومعالجته كأي أمر آخر.</span><span class="sxs-lookup"><span data-stu-id="dde9f-117">The purchase order can now be completed and processed like any other order.</span></span> <span data-ttu-id="dde9f-118">لا توجد أية سمات خاصة تتعلق بكيفية إجراء ذلك.</span><span class="sxs-lookup"><span data-stu-id="dde9f-118">There are no special characteristics related to how this is done.</span></span> <span data-ttu-id="dde9f-119">ستحسب الفاتورة حركة مستحقة على حساب المورّد الذي تم إنشاؤه باستخدام الأمر، وستتم معالجة الدفع عندئذٍ.</span><span class="sxs-lookup"><span data-stu-id="dde9f-119">The invoice will account a due transaction on the vendor account that was created with the order, and payment will then be processed.</span></span>

