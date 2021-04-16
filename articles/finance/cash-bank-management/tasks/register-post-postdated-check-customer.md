---
title: تسجيل شيك بتاريخ لاحق لعميل وترحيله
description: يمكنك تسجيل التفاصيل لشيك بتاريخ لاحق تم استلامه من عميل.
author: kweekley
ms.date: 10/26/2017
ms.topic: business-process
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 9cb49ac6ebbd04e71215af010cb5a7b6302fe44e
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 04/01/2021
ms.locfileid: "5834682"
---
# <a name="register-and-post-a-postdated-check-for-a-customer"></a><span data-ttu-id="9bf80-103">تسجيل شيك بتاريخ لاحق لعميل وترحيله</span><span class="sxs-lookup"><span data-stu-id="9bf80-103">Register and post a postdated check for a customer</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="9bf80-104">يمكنك تسجيل التفاصيل لشيك بتاريخ لاحق تم استلامه من عميل.</span><span class="sxs-lookup"><span data-stu-id="9bf80-104">You can register details of a postdated check received from a customer.</span></span> <span data-ttu-id="9bf80-105">ويمكنك أيضا ترحيل الشيك الذي تم تأخير تاريخه وإنشاء الحركات المالية.</span><span class="sxs-lookup"><span data-stu-id="9bf80-105">You can also post the postdated check and generate financial transactions.</span></span>   <span data-ttu-id="9bf80-106">أكمل المهام التالية قبل تسجيل وترحيل الشيكات الواردة من عميل بتاريخ لاحق:   \* إعداد شيكات بتاريخ لاحق في صفحة إدارة النقد والبنوك \* إعداد طريقة دفع للشيكات بتاريخ لاحق   أمين الخزانة هو الشخص المنوط به هذا الدور.</span><span class="sxs-lookup"><span data-stu-id="9bf80-106">Complete the following tasks before you register and post a postdated check received from a customer:   \* Set up postdated check in the Cash and bank management page \* Set up a method of payment for postdated checks   The role for this procedure is Treasurer.</span></span> <span data-ttu-id="9bf80-107">يستخدم هذا الإجراء شركة بيانات العرض التوضيحي USMF.</span><span class="sxs-lookup"><span data-stu-id="9bf80-107">This procedure uses the USMF demo company.</span></span>

1. <span data-ttu-id="9bf80-108">انتقل إلى الحسابات المدينة > المدفوعات‬ > دفتر يومية المدفوعات‬‬.</span><span class="sxs-lookup"><span data-stu-id="9bf80-108">Go to Accounts receivable > Payments > Payment journal.</span></span>
2. <span data-ttu-id="9bf80-109">انقر فوق "جديد".</span><span class="sxs-lookup"><span data-stu-id="9bf80-109">Click New.</span></span>
3. <span data-ttu-id="9bf80-110">في حقل "الاسم"، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="9bf80-110">In the Name field, type a value.</span></span>
4. <span data-ttu-id="9bf80-111">انقر فوق البنود.</span><span class="sxs-lookup"><span data-stu-id="9bf80-111">Click Lines.</span></span>
5. <span data-ttu-id="9bf80-112">في القائمة، قم بوضع علامة للصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="9bf80-112">In the list, mark the selected row.</span></span>
6. <span data-ttu-id="9bf80-113">في حقل "الحساب"، حدد القيم المطلوبة.</span><span class="sxs-lookup"><span data-stu-id="9bf80-113">In the Account field, specify the desired values.</span></span>
7. <span data-ttu-id="9bf80-114">في الحقل "دائن"، أدخل رقمًا.</span><span class="sxs-lookup"><span data-stu-id="9bf80-114">In the Credit field, enter a number.</span></span>
    * <span data-ttu-id="9bf80-115">أدخل المبلغ المحدد في الشيك الذي تم تأخير تاريخه.</span><span class="sxs-lookup"><span data-stu-id="9bf80-115">Enter the amount specified in the postdated check.</span></span>  
8. <span data-ttu-id="9bf80-116">انقر فوق علامة التبويب "الدفع".</span><span class="sxs-lookup"><span data-stu-id="9bf80-116">Click the Payment tab.</span></span>
9. <span data-ttu-id="9bf80-117">في الحقل "طريقة الدفع"، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="9bf80-117">In the Method of payment field, type a value.</span></span>
    * <span data-ttu-id="9bf80-118">حدد طريقة دفع الشيك الذي تم تأخير تاريخه.</span><span class="sxs-lookup"><span data-stu-id="9bf80-118">Select the method of payment for the postdated check.</span></span>  
10. <span data-ttu-id="9bf80-119">انقر فوق علامة التبويب "الشيكات التي تم تأخير تواريخها".</span><span class="sxs-lookup"><span data-stu-id="9bf80-119">Click the Postdated checks tab.</span></span>
11. <span data-ttu-id="9bf80-120">في الحقل "تاريخ الاستحقاق"، أدخل تاريخًا.</span><span class="sxs-lookup"><span data-stu-id="9bf80-120">In the Maturity date field, enter a date.</span></span>
    * <span data-ttu-id="9bf80-121">أدخل تاريخ استحقاق الشيك الذي تم تأخير تاريخه للدفع.</span><span class="sxs-lookup"><span data-stu-id="9bf80-121">Enter the date when the postdated check is due for payment.</span></span>  
12. <span data-ttu-id="9bf80-122">في الحقل "فرع بنك الإصدار"، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="9bf80-122">In the Issuing bank branch field, type a value.</span></span>
    * <span data-ttu-id="9bf80-123">أدخل تفاصيل البنك للشيك الذي تم تأخير تاريخه.</span><span class="sxs-lookup"><span data-stu-id="9bf80-123">Enter the bank details of the postdated check.</span></span>  
13. <span data-ttu-id="9bf80-124">في الحقل "رقم الشيك"، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="9bf80-124">In the check number field, type a value.</span></span>
14. <span data-ttu-id="9bf80-125">في الحقل "اسم بنك الإصدار"، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="9bf80-125">In the Issuing bank name field, type a value.</span></span>
    * <span data-ttu-id="9bf80-126">أدخل تفاصيل البنك للشيك الذي تم تأخير تاريخه.</span><span class="sxs-lookup"><span data-stu-id="9bf80-126">Enter the bank details of the postdated check.</span></span>  
15. <span data-ttu-id="9bf80-127">انقر فوق "ترحيل".</span><span class="sxs-lookup"><span data-stu-id="9bf80-127">Click Post.</span></span>
16. <span data-ttu-id="9bf80-128">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="9bf80-128">Close the page.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]