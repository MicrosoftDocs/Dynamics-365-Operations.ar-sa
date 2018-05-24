---
title: "إدارة الأصناف المقرضة للعاملين"
description: "أصناف القرض هي سجلات تساعد المديرين على تعقب الأصناف الفعلية التي تقوم شركتك بإعارتها للعاملين."
author: kherr75
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-365-talent
ms.technology: 
ms.search.form: HcmLoanItem, HcmLoanType, HcmPersonLoan
audience: Application User
ms.reviewer: rschloma
ms.search.scope: Core, Operations, Talent
ms.custom: 3581
ms.assetid: b14bdddb-f10e-4619-9f91-8c88439da862
ms.search.region: Global
ms.author: kherr
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Talent July 2017 update
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: fe8d8812aaa78c7b5558615f586940488f2dc1b2
ms.contentlocale: ar-sa
ms.lasthandoff: 05/08/2018

---

# <a name="manage-items-lent-to-workers"></a><span data-ttu-id="ac088-103">إدارة الأصناف المقرضة للعاملين</span><span class="sxs-lookup"><span data-stu-id="ac088-103">Manage items lent to workers</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="ac088-104">أصناف القرض هي سجلات تساعد المديرين على تعقب الأصناف الفعلية التي تقوم شركتك بإعارتها للعاملين.</span><span class="sxs-lookup"><span data-stu-id="ac088-104">Loan items are records that help managers track the physical items that your company lends to its workers.</span></span> 

<span data-ttu-id="ac088-105">تسرد قائمة النقاط التالية أمثلة للأصناف التي قد تقرضها شركة للعاملين:</span><span class="sxs-lookup"><span data-stu-id="ac088-105">The following points list examples of items that a company might lend to workers:</span></span>
-   <span data-ttu-id="ac088-106">الهواتف المحمولة</span><span class="sxs-lookup"><span data-stu-id="ac088-106">Mobile telephones</span></span>
-   <span data-ttu-id="ac088-107">السيارات</span><span class="sxs-lookup"><span data-stu-id="ac088-107">Automobiles</span></span>
-   <span data-ttu-id="ac088-108">أجهزة الكمبيوتر</span><span class="sxs-lookup"><span data-stu-id="ac088-108">Computer equipment</span></span>

<span data-ttu-id="ac088-109">يجب أن يكون لكل عنصر فعلي صنف قرض مناظر.</span><span class="sxs-lookup"><span data-stu-id="ac088-109">Each physical item must have a corresponding loan item.</span></span> <span data-ttu-id="ac088-110">يجب أن يصف كل سجل لأصناف القرض ما الصنف الذي يتم إقراضه والشخص المسؤول عن القرض وعدد الأيام التي يمكن إقراض الصنف فيها للعامل.</span><span class="sxs-lookup"><span data-stu-id="ac088-110">Each loan item record should describe what is being loaned, who is responsible for the loan, and the number of days the item can loaned to a worker.</span></span> <span data-ttu-id="ac088-111">ويمكنك إنشاء أصناف قرض متعددة للأصنف، مثل المفاتيح أو بطاقات الدخول أو الزي الموحد، في نفس الوقت.</span><span class="sxs-lookup"><span data-stu-id="ac088-111">You can create multiple loan items, for items such as keys, access cards or uniforms, at the same time.</span></span> 

<span data-ttu-id="ac088-112">عند إقراض أحد الأصناف، أدخل تاريخ إقراض الصنف وكذلك تاريخ الإرجاع المخطط.</span><span class="sxs-lookup"><span data-stu-id="ac088-112">When loaning an item, enter the date that the item was loaned, and the planned return date.</span></span> <span data-ttu-id="ac088-113">وعند إرجاع الصنف، أدخل تاريخ الإرجاع الفعلي.</span><span class="sxs-lookup"><span data-stu-id="ac088-113">When the item is returned, enter the actual return date.</span></span>

<span data-ttu-id="ac088-114">يمكن للموظفين عرض السجلات الخاصة بالأصناف التي تم إقراضها لهم باستخدام مساحة الخدمة الذاتية للموظف.</span><span class="sxs-lookup"><span data-stu-id="ac088-114">Employees can view the records of the items that have been loaned to them using the Employee self-service workspace.</span></span> <span data-ttu-id="ac088-115">‏‫كما يمكنهم أيضًا تحرير سجلات موجودة أو إدخال أصناف قرض جديدة، إذا تلقيت أصناف إضافية فعلية.</span><span class="sxs-lookup"><span data-stu-id="ac088-115">They can also edit the existing records or enter new loan items, if they've received additional physical items.</span></span>  <span data-ttu-id="ac088-116">ويمكن إعداد سير عمل لتوجيه تغييرات لأصناف قرض جديدة أو موجودة من خلال عملية موافقة.‬‏‫</span><span class="sxs-lookup"><span data-stu-id="ac088-116">Workflow can be set up to route changes to new or existing loan items through an approval process.</span></span> 

<span data-ttu-id="ac088-117">يمكن للمديرين عرض الأصناف المُقرضة لتقاريرهم المباشرة.</span><span class="sxs-lookup"><span data-stu-id="ac088-117">Managers can view loaned items for their direct reports.</span></span> <span data-ttu-id="ac088-118">كما يمكنهم منح الإذن لإضافة أصناف قرض جديدة بالنيابة عن موظفيهم.</span><span class="sxs-lookup"><span data-stu-id="ac088-118">They can also be granted permission to add new loan items on behalf of their employees.</span></span>

 <a name="account-for-lost-or-misplaced-loan-items"></a><span data-ttu-id="ac088-119"> الحساب الخاص بأصناف القرض المفقودة أو الموضوعة في غير موضعها</span><span class="sxs-lookup"><span data-stu-id="ac088-119">Account for lost or misplaced loan items</span></span>
-----------------------------------------

<span data-ttu-id="ac088-120">في حالة تعرض أحد الأصناف للتلف أو تم وضعه في غير موضعه، أدخل سجل إرجاع وهمي.</span><span class="sxs-lookup"><span data-stu-id="ac088-120">If an item becomes damaged or misplaced, enter a fictitious return record.</span></span> <span data-ttu-id="ac088-121">ثم قم إما بحذف الصنف أو بإبقائه في النظرة العامة وتغيير الوصف للإشارة إلى أن الصنف غير متاح.</span><span class="sxs-lookup"><span data-stu-id="ac088-121">Then either delete the item or keep it in the overview and change the description to indicate that the item is not available.</span></span>


<a name="additional-resources"></a><span data-ttu-id="ac088-122">الموارد الإضافية</span><span class="sxs-lookup"><span data-stu-id="ac088-122">Additional resources</span></span>
--------

[<span data-ttu-id="ac088-123">الموارد البشرية</span><span class="sxs-lookup"><span data-stu-id="ac088-123">Human resources</span></span>](index.md)




