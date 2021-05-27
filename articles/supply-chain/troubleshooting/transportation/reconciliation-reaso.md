---
title: يمكنك إضافة الحساب الرئيسي فقط كحساب دائن لأسباب التسوية
description: عندما تقوم بإعداد سبب تسوية في إدارة النقل، يمكنك إضافة الحساب الرئيسي فقط كحساب دائن.
author: Henrikan
ms.date: 4/11/2021
ms.topic: troubleshooting
ms.search.form: TMSFBDetailReconcile
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: henrikan
ms.search.validFrom: 2021-04-11
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: 708081370b27fd51ef9a2329d8392f4515353dcb
ms.sourcegitcommit: c011a2ef66b38e71ddaf003f7d243677bb2707c5
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 05/12/2021
ms.locfileid: "6026221"
---
# <a name="you-can-add-only-the-main-account-as-the-credit-account-for-reconciliation-reasons"></a><span data-ttu-id="e20fa-103">يمكنك إضافة الحساب الرئيسي فقط كحساب دائن لأسباب التسوية</span><span class="sxs-lookup"><span data-stu-id="e20fa-103">You can add only the main account as the credit account for reconciliation reasons</span></span>

<span data-ttu-id="e20fa-104">رقم KB: 4603538</span><span class="sxs-lookup"><span data-stu-id="e20fa-104">KB number: 4603538</span></span>

## <a name="symptoms"></a><span data-ttu-id="e20fa-105">العلامات</span><span class="sxs-lookup"><span data-stu-id="e20fa-105">Symptoms</span></span>

<span data-ttu-id="e20fa-106">عندما تقوم بإعداد سبب تسوية في إدارة النقل، يمكنك إضافة الحساب الرئيسي فقط كحساب دائن.</span><span class="sxs-lookup"><span data-stu-id="e20fa-106">When you set up a reconciliation reason in Transportation management, you can add only the main account as the credit account.</span></span> <span data-ttu-id="e20fa-107">لا يمكنك إضافة مركز التكلفة أو أي بعد آخر كحساب دائن.</span><span class="sxs-lookup"><span data-stu-id="e20fa-107">You can't add a cost center or any other dimension as the credit account.</span></span> <span data-ttu-id="e20fa-108">ومع ذلك، يتيح لك حساب المدين تحديد أبعاد أخرى.</span><span class="sxs-lookup"><span data-stu-id="e20fa-108">However, the debit account lets you select other dimensions.</span></span>

## <a name="resolution"></a><span data-ttu-id="e20fa-109">الدقة</span><span class="sxs-lookup"><span data-stu-id="e20fa-109">Resolution</span></span>

<span data-ttu-id="e20fa-110">إذا لم يتم إجراء التسوية لدفع المورد ولكن بالإضافة إلى حساب رئيسي محدد، فلن يسمح النظام بتحديد بُعد مالي لحساب الدائن عند إعداد سبب التسوية.</span><span class="sxs-lookup"><span data-stu-id="e20fa-110">If the reconciliation isn't done to pay the vendor but to credit a specific main account, the system doesn't allow you to select a financial dimension for the credit account when you set up the reconciliation reason.</span></span>

<span data-ttu-id="e20fa-111">إذا كانت بنية الحساب تتطلب قيمة بُعد مالي معينة لحساب الدائن الرئيسي، فلا يمكن ترحيل دفتر يومية المورد الناتج تلقائيًا، لأن قيمة البُعد المالي مفقودة.</span><span class="sxs-lookup"><span data-stu-id="e20fa-111">If the account structure requires a specific financial dimension value for the credit main account, the resulting vendor journal can't be posted automatically, because the financial dimension value is missing.</span></span> <span data-ttu-id="e20fa-112">وبالتالي، يجب أولاً تحديد الحساب الدائن يدويًا باستخدام الصفحة **دفتر يومية الفواتير**.</span><span class="sxs-lookup"><span data-stu-id="e20fa-112">Therefore, you must first manually specify the credit account by using the **Invoice journal** page.</span></span>

<span data-ttu-id="e20fa-113">ونظرًا لأن قيمة البُعد مطلوبة للحساب الدائن، فلا يمكن ترحيل دفتر يومية فاتورة المورد تلقائيًا.</span><span class="sxs-lookup"><span data-stu-id="e20fa-113">Because a dimension value is required for the credit account, the vendor invoice journal can't be automatically posted.</span></span> <span data-ttu-id="e20fa-114">يجب ترحيلها يدويًا بعد إضافة قيمة البُعد يدويًا إلى الحساب الرئيسي لبند الدائن.</span><span class="sxs-lookup"><span data-stu-id="e20fa-114">You must manually post it after you manually add the dimension value to the main account for the credit line.</span></span>
