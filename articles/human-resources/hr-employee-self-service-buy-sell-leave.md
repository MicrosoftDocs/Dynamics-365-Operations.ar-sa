---
title: شراء الإجازة وبيعها
description: في Dynamics 365 Human Resources ، يمكن إرسال طلبات لشراء الإجازة وبيعها استنادًا إلى إعداد سياسات شراء وبيع الإجازات الخاص بشركتك.
author: andreabichsel
ms.date: 08/20/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ESSLeaveBuyRequestEntry, EssWorkspace
audience: Application User
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-06-01
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 6d32abacc1539cb930ad6f1ebcfe6fa9af4befcf
ms.sourcegitcommit: dc4898aa32f381620c517bf89c7856e693563ace
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 06/17/2021
ms.locfileid: "6271464"
---
# <a name="buy-and-sell-leave"></a><span data-ttu-id="77bdf-103">شراء الإجازة وبيعها</span><span class="sxs-lookup"><span data-stu-id="77bdf-103">Buy and sell leave</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="77bdf-104">في Dynamics 365 Human Resources ، يمكن إرسال طلبات لشراء الإجازة وبيعها استنادًا إلى إعداد سياسات شراء وبيع الإجازات الخاص بشركتك.</span><span class="sxs-lookup"><span data-stu-id="77bdf-104">In Dynamics 365 Human Resources, you can submit requests to buy and sell leave based on the buy and sell leave policies set up by your company.</span></span>  

## <a name="request-to-buy-leave"></a><span data-ttu-id="77bdf-105">طلب شراء إجازة</span><span class="sxs-lookup"><span data-stu-id="77bdf-105">Request to buy leave</span></span>

1. <span data-ttu-id="77bdf-106">في مساحة عمل **خدمة الموظف الذاتية** حدد **طلب شراء إجازة** في اللوحة **أرصدة زمن التوقف**.</span><span class="sxs-lookup"><span data-stu-id="77bdf-106">In the **Employee self service** workspace, select **Buy leave request** in the **Time Off Balances** tile.</span></span> 

2. <span data-ttu-id="77bdf-107">أضف **نوع إجازة** وفي حقل **المقدار** أدخل مقدار الإجازة الذي ترغب في شرائه.</span><span class="sxs-lookup"><span data-stu-id="77bdf-107">Add a **Leave type** and enter an **Amount** for the amount of leave you'd like to buy.</span></span> 

3. <span data-ttu-id="77bdf-108">حدد **إرسال** عندما تكون مستعدا لتقديم طلبك.</span><span class="sxs-lookup"><span data-stu-id="77bdf-108">Select **Submit** when you're ready to submit your request.</span></span> 

<span data-ttu-id="77bdf-109">سيتم إما تحديث رصيدك تلقائيًا أو المرور بعملية اعتماد قبل التحديث.</span><span class="sxs-lookup"><span data-stu-id="77bdf-109">Your balances will either automatically update or go through an approval process before updating.</span></span> <span data-ttu-id="77bdf-110">ويعتمد ذلك علي كيفية تكوين سياسة الشراء.</span><span class="sxs-lookup"><span data-stu-id="77bdf-110">This depends on how the buy policy has been configured.</span></span>

## <a name="request-to-sell-leave"></a><span data-ttu-id="77bdf-111">طلب بيع إجازة</span><span class="sxs-lookup"><span data-stu-id="77bdf-111">Request to sell leave</span></span>

1. <span data-ttu-id="77bdf-112">في مساحة عمل **خدمة الموظف الذاتية** حدد **طلب بيع إجازة** في اللوحة **أرصدة زمن التوقف**.</span><span class="sxs-lookup"><span data-stu-id="77bdf-112">In the **Employee self service** workspace, select **Sell leave request** in the **Time Off Balances** tile.</span></span> 

2. <span data-ttu-id="77bdf-113">أضف **نوع إجازة** وفي حقل **المقدار** أدخل مقدار الإجازة الذي ترغب في بيعه.</span><span class="sxs-lookup"><span data-stu-id="77bdf-113">Add a **Leave type** and enter an **Amount** for the amount of leave you'd like to sell.</span></span> 

3. <span data-ttu-id="77bdf-114">حدد **إرسال** عندما تكون مستعدا لتقديم طلبك.</span><span class="sxs-lookup"><span data-stu-id="77bdf-114">Select **Submit** when you're ready to submit your request.</span></span>

<span data-ttu-id="77bdf-115">سيتم إما تحديث رصيدك تلقائيًا أو المرور بعملية اعتماد قبل التحديث.</span><span class="sxs-lookup"><span data-stu-id="77bdf-115">Your balances will either automatically update or go through an approval process before updating.</span></span> <span data-ttu-id="77bdf-116">ويعتمد ذلك علي كيفية تكوين سياسة الشراء.</span><span class="sxs-lookup"><span data-stu-id="77bdf-116">This depends on how the buy policy has been configured.</span></span>


## <a name="troubleshooting"></a><span data-ttu-id="77bdf-117">استكشاف الأخطاء وإصلاحها</span><span class="sxs-lookup"><span data-stu-id="77bdf-117">Troubleshooting</span></span> 

<span data-ttu-id="77bdf-118">في حالة فشل سير عمل طلب شراء أو بيع، يمكن للمستخدمين الذين لديهم الامتياز **EssLeaveBuySellRequestApprover** مراجعة سجل الرسائل لكافة طلبات الشراء والبيع.</span><span class="sxs-lookup"><span data-stu-id="77bdf-118">If a buy or sell leave request workflow fails, users with the **EssLeaveBuySellRequestApprover** privilege can review the message log for all leave buy and sell requests.</span></span> <span data-ttu-id="77bdf-119">للقيام بذلك، انتقل إلى **الإجازة والغياب > الارتباط > طلبات شراء وبيع الإجازة > سجل الرسائل** (في الجانب العلوي الأيسر).</span><span class="sxs-lookup"><span data-stu-id="77bdf-119">To do this, go to **Leave and absence > Link > Buy and sell leave requests > Message log** (on the upper left).</span></span> <span data-ttu-id="77bdf-120">يعرض **سجل الرسائل** للمستخدمين كيفية معالجة الحركات ومحفوظات سير العمل المرتبطة.</span><span class="sxs-lookup"><span data-stu-id="77bdf-120">The **Message log** shows users how the transactions were processed and the associated workflow history.</span></span>


## <a name="see-also"></a><span data-ttu-id="77bdf-121">راجع أيضًا</span><span class="sxs-lookup"><span data-stu-id="77bdf-121">See also</span></span>

[<span data-ttu-id="77bdf-122">نظرة عامة على الإجازة والغياب</span><span class="sxs-lookup"><span data-stu-id="77bdf-122">Leave and absence overview</span></span>](hr-leave-and-absence-overview.md)</br>
[<span data-ttu-id="77bdf-123">إدارة سياسات شراء الإجازة وبيعها</span><span class="sxs-lookup"><span data-stu-id="77bdf-123">Manage buy and sell leave policies</span></span>](hr-leave-and-absence-manage-buy-and-sell-leave-policies.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
