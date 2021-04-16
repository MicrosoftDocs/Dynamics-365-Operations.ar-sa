---
title: إنشاء اتفاقية تسهيلات مصرفية لخطاب الاعتماد
description: تنقلك هذه المهمة عبر عملية إنشاء اتفاقية التسهيلات البنكية‬ لمعالجة خطاب اعتماد.
author: ShylaThompson
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: BankDocumentFacilityAgreement, BankAccountTableLookUp, BankDocumentFacilityAgreementExtension, DefaultDashboard
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: leguo
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 582a41a0a4a3c509eae8a05c57b0910446addb26
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 04/01/2021
ms.locfileid: "5834826"
---
# <a name="create-a-bank-facility-agreement-for-a-letter-of-credit"></a><span data-ttu-id="e3ccc-103">إنشاء اتفاقية تسهيلات مصرفية لخطاب الاعتماد</span><span class="sxs-lookup"><span data-stu-id="e3ccc-103">Create a bank facility agreement for a letter of credit</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="e3ccc-104">تنقلك هذه المهمة عبر عملية إنشاء اتفاقية التسهيلات البنكية‬ لمعالجة خطاب اعتماد.</span><span class="sxs-lookup"><span data-stu-id="e3ccc-104">This task walks through the creating a Bank facility agreement to process a Letter of credit.</span></span> <span data-ttu-id="e3ccc-105">ستحتاج إلى إعداد التسهيلات البنكية وملفات تعريف الترحيل قبل هذه المهمة.</span><span class="sxs-lookup"><span data-stu-id="e3ccc-105">You will want to set up bank facilities and posting profiles before this task.</span></span>  <span data-ttu-id="e3ccc-106">تستخدم هذه المهمة شركة بيانات العرض التوضيحي USMF.</span><span class="sxs-lookup"><span data-stu-id="e3ccc-106">This task uses the demo company 'USMF'.</span></span>  


## <a name="create-bank-facility-agreement"></a><span data-ttu-id="e3ccc-107">إنشاء اتفاقية التسهيلات البنكية</span><span class="sxs-lookup"><span data-stu-id="e3ccc-107">Create Bank facility agreement</span></span>
1. <span data-ttu-id="e3ccc-108">انتقل إلى إدارة النقد والبنوك > خطابات الاعتماد > اتفاقيات التسهيلات البنكية‬.</span><span class="sxs-lookup"><span data-stu-id="e3ccc-108">Go to Cash and bank management > Letters of credit > Bank facility agreements.</span></span>
2. <span data-ttu-id="e3ccc-109">انقر فوق "جديد".</span><span class="sxs-lookup"><span data-stu-id="e3ccc-109">Click New.</span></span>
3. <span data-ttu-id="e3ccc-110">في الحقل "رقم الاتفاقية"، أدخل رقم الاتفاقية وفقًا للاتفاقية المعقودة مع البنك.</span><span class="sxs-lookup"><span data-stu-id="e3ccc-110">In the Agreement number field, enter the agreement number according to the agreement with the bank.</span></span>
4. <span data-ttu-id="e3ccc-111">في الحقل "حساب البنك‬"، أدخل رقم حساب البنك في البنك المصدر.</span><span class="sxs-lookup"><span data-stu-id="e3ccc-111">In the Bank account field, enter the account number at the issuing bank.</span></span>
5. <span data-ttu-id="e3ccc-112">في القائمة، انقر فوق الارتباط في الصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="e3ccc-112">In the list, click the link in the selected row.</span></span>
6. <span data-ttu-id="e3ccc-113">في الحقل "تاريخ البدء"، أدخل تاريخًا ووقتًا.</span><span class="sxs-lookup"><span data-stu-id="e3ccc-113">In the Start date field, enter a date and time.</span></span>
7. <span data-ttu-id="e3ccc-114">في الحقل "تاريخ الانتهاء"، أدخل تاريخًا ووقتًا.</span><span class="sxs-lookup"><span data-stu-id="e3ccc-114">In the End date field, enter a date and time.</span></span>
8. <span data-ttu-id="e3ccc-115">قم بتوسيع أو طي المقطع "عام".</span><span class="sxs-lookup"><span data-stu-id="e3ccc-115">Expand or collapse the General section.</span></span>
9. <span data-ttu-id="e3ccc-116">انقر فوق "إضافة بند".</span><span class="sxs-lookup"><span data-stu-id="e3ccc-116">Click Add line.</span></span>
10. <span data-ttu-id="e3ccc-117">في الحقل "نوع التسهيلات‬"، انقر فوق زر القائمة المنسدلة لفتح البحث.</span><span class="sxs-lookup"><span data-stu-id="e3ccc-117">In the Facility type field, click the drop-down button to open the lookup.</span></span>
11. <span data-ttu-id="e3ccc-118">في القائمة، قم بالبحث عن السجل المطلوب وحدده.</span><span class="sxs-lookup"><span data-stu-id="e3ccc-118">In the list, find and select the desired record.</span></span>
12. <span data-ttu-id="e3ccc-119">في القائمة، انقر فوق الارتباط في الصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="e3ccc-119">In the list, click the link in the selected row.</span></span>
13. <span data-ttu-id="e3ccc-120">في الحقل "الحد"، أدخل مبلغ التسهيلات الذي تم التفاوض عليه مع البنك.</span><span class="sxs-lookup"><span data-stu-id="e3ccc-120">In the Limit field, enter the facility amount that was negotiated with the bank.</span></span>
14. <span data-ttu-id="e3ccc-121">انقر فوق حفظ.</span><span class="sxs-lookup"><span data-stu-id="e3ccc-121">Click Save.</span></span>
15. <span data-ttu-id="e3ccc-122">انقر فوق "توسيع‬" لفتح مربع حوار الإسقاط‬.</span><span class="sxs-lookup"><span data-stu-id="e3ccc-122">Click Extend to open the drop dialog.</span></span>
16. <span data-ttu-id="e3ccc-123">في الحقل "رقم اتفاقية جديد‬"، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="e3ccc-123">In the New agreement number field, type a value.</span></span>
17. <span data-ttu-id="e3ccc-124">في الحقل "تاريخ الانتهاء"، أدخل تاريخًا ووقتًا.</span><span class="sxs-lookup"><span data-stu-id="e3ccc-124">In the End date field, enter a date and time.</span></span>
18. <span data-ttu-id="e3ccc-125">انقر فوق "توسيع".</span><span class="sxs-lookup"><span data-stu-id="e3ccc-125">Click Extend.</span></span>
19. <span data-ttu-id="e3ccc-126">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="e3ccc-126">Close the page.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]