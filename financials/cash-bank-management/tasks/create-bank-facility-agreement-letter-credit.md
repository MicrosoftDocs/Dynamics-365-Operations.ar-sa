--- 
title: "إنشاء اتفاقية تسهيلات مصرفية لخطاب الاعتماد"
description: "تنقلك هذه المهمة عبر عملية إنشاء اتفاقية التسهيلات البنكية‬ لمعالجة خطاب اعتماد."
author: ShylaThompson
manager: AnnBe
ms.date: 02/10/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Operations
ms.search.region: Global
ms.author: leguo
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: ac3394a40bff3aaee6a76448633e4f36c4049612
ms.contentlocale: ar-sa
ms.lasthandoff: 08/29/2017

---
# <a name="create-a-bank-facility-agreement-for-a-letter-of-credit"></a><span data-ttu-id="7c844-103">إنشاء اتفاقية تسهيلات مصرفية لخطاب الاعتماد</span><span class="sxs-lookup"><span data-stu-id="7c844-103">Create a bank facility agreement for a letter of credit</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="7c844-104">تنقلك هذه المهمة عبر عملية إنشاء اتفاقية التسهيلات البنكية‬ لمعالجة خطاب اعتماد.</span><span class="sxs-lookup"><span data-stu-id="7c844-104">This task walks through the creating a Bank facility agreement to process a Letter of credit.</span></span> <span data-ttu-id="7c844-105">ستحتاج إلى إعداد التسهيلات البنكية وملفات تعريف الترحيل قبل هذه المهمة.</span><span class="sxs-lookup"><span data-stu-id="7c844-105">You will want to set up bank facilities and posting profiles before this task.</span></span>  <span data-ttu-id="7c844-106">تستخدم هذه المهمة شركة بيانات العرض التوضيحي USMF.</span><span class="sxs-lookup"><span data-stu-id="7c844-106">This task uses the demo company 'USMF'.</span></span>  


## <a name="create-bank-facility-agreement"></a><span data-ttu-id="7c844-107">إنشاء اتفاقية التسهيلات البنكية</span><span class="sxs-lookup"><span data-stu-id="7c844-107">Create Bank facility agreement</span></span>
1. <span data-ttu-id="7c844-108">انتقل إلى إدارة النقد والبنوك > خطابات الاعتماد > اتفاقيات التسهيلات البنكية‬.</span><span class="sxs-lookup"><span data-stu-id="7c844-108">Go to Cash and bank management > Letters of credit > Bank facility agreements.</span></span>
2. <span data-ttu-id="7c844-109">انقر فوق "جديد".</span><span class="sxs-lookup"><span data-stu-id="7c844-109">Click New.</span></span>
3. <span data-ttu-id="7c844-110">في الحقل "رقم الاتفاقية"، أدخل رقم الاتفاقية وفقًا للاتفاقية المعقودة مع البنك.</span><span class="sxs-lookup"><span data-stu-id="7c844-110">In the Agreement number field, enter the agreement number according to the agreement with the bank.</span></span>
4. <span data-ttu-id="7c844-111">في الحقل "حساب البنك‬"، أدخل رقم حساب البنك في البنك المصدر.</span><span class="sxs-lookup"><span data-stu-id="7c844-111">In the Bank account field, enter the account number at the issuing bank.</span></span>
5. <span data-ttu-id="7c844-112">في القائمة، انقر فوق الارتباط في الصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="7c844-112">In the list, click the link in the selected row.</span></span>
6. <span data-ttu-id="7c844-113">في الحقل "تاريخ البدء"، أدخل تاريخًا ووقتًا.</span><span class="sxs-lookup"><span data-stu-id="7c844-113">In the Start date field, enter a date and time.</span></span>
7. <span data-ttu-id="7c844-114">في الحقل "تاريخ الانتهاء"، أدخل تاريخًا ووقتًا.</span><span class="sxs-lookup"><span data-stu-id="7c844-114">In the End date field, enter a date and time.</span></span>
8. <span data-ttu-id="7c844-115">قم بتوسيع أو طي المقطع "عام".</span><span class="sxs-lookup"><span data-stu-id="7c844-115">Expand or collapse the General section.</span></span>
9. <span data-ttu-id="7c844-116">انقر فوق "إضافة بند".</span><span class="sxs-lookup"><span data-stu-id="7c844-116">Click Add line.</span></span>
10. <span data-ttu-id="7c844-117">في الحقل "نوع التسهيلات‬"، انقر فوق زر القائمة المنسدلة لفتح البحث.</span><span class="sxs-lookup"><span data-stu-id="7c844-117">In the Facility type field, click the drop-down button to open the lookup.</span></span>
11. <span data-ttu-id="7c844-118">في القائمة، قم بالبحث عن السجل المطلوب وحدده.</span><span class="sxs-lookup"><span data-stu-id="7c844-118">In the list, find and select the desired record.</span></span>
12. <span data-ttu-id="7c844-119">في القائمة، انقر فوق الارتباط في الصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="7c844-119">In the list, click the link in the selected row.</span></span>
13. <span data-ttu-id="7c844-120">في الحقل "الحد"، أدخل مبلغ التسهيلات الذي تم التفاوض عليه مع البنك.</span><span class="sxs-lookup"><span data-stu-id="7c844-120">In the Limit field, enter the facility amount that was negotiated with the bank.</span></span>
14. <span data-ttu-id="7c844-121">انقر فوق حفظ.</span><span class="sxs-lookup"><span data-stu-id="7c844-121">Click Save.</span></span>
15. <span data-ttu-id="7c844-122">انقر فوق "توسيع‬" لفتح مربع حوار الإسقاط‬.</span><span class="sxs-lookup"><span data-stu-id="7c844-122">Click Extend to open the drop dialog.</span></span>
16. <span data-ttu-id="7c844-123">في الحقل "رقم اتفاقية جديد‬"، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="7c844-123">In the New agreement number field, type a value.</span></span>
17. <span data-ttu-id="7c844-124">في الحقل "تاريخ الانتهاء"، أدخل تاريخًا ووقتًا.</span><span class="sxs-lookup"><span data-stu-id="7c844-124">In the End date field, enter a date and time.</span></span>
18. <span data-ttu-id="7c844-125">انقر فوق "توسيع".</span><span class="sxs-lookup"><span data-stu-id="7c844-125">Click Extend.</span></span>
19. <span data-ttu-id="7c844-126">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="7c844-126">Close the page.</span></span>


