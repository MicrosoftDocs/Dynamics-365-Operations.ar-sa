---
title: إدارة الأصناف المعارة للعاملين
description: أصناف القرض هي سجلات تساعد المديرين على تعقب الأصناف الفعلية التي تقوم شركتك بإعارتها للعاملين.
author: andreabichsel
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-human-resources
ms.technology: ''
ms.search.form: HcmLoanItem, HcmLoanType, HcmPersonLoan
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Core, Operations, Human Resources
ms.custom: 3581
ms.assetid: b14bdddb-f10e-4619-9f91-8c88439da862
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Human Resources
ms.openlocfilehash: 02382872b685103810dd7e84cb91eb409df62f66
ms.sourcegitcommit: 880f617d1d6e95eccbed762c7ea04398553c2ec0
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 02/11/2020
ms.locfileid: "3036301"
---
# <a name="manage-items-that-are-lent-to-workers"></a><span data-ttu-id="22238-103">إدارة الأصناف المعارة للعاملين</span><span class="sxs-lookup"><span data-stu-id="22238-103">Manage items that are lent to workers</span></span>

<span data-ttu-id="22238-104">أصناف القرض هي سجلات تساعد المديرين على تعقب الأصناف الفعلية التي تقوم شركتك بإعارتها للعاملين.</span><span class="sxs-lookup"><span data-stu-id="22238-104">Loan items are records that help managers track the physical items that your company lends to its workers.</span></span> 

<span data-ttu-id="22238-105">تسرد قائمة النقاط التالية أمثلة للأصناف التي قد تقرضها شركة للعاملين:</span><span class="sxs-lookup"><span data-stu-id="22238-105">The following points list examples of items that a company might lend to workers:</span></span>
-   <span data-ttu-id="22238-106">الهواتف المحمولة</span><span class="sxs-lookup"><span data-stu-id="22238-106">Mobile telephones</span></span>
-   <span data-ttu-id="22238-107">السيارات</span><span class="sxs-lookup"><span data-stu-id="22238-107">Automobiles</span></span>
-   <span data-ttu-id="22238-108">أجهزة الكمبيوتر</span><span class="sxs-lookup"><span data-stu-id="22238-108">Computer equipment</span></span>

<span data-ttu-id="22238-109">يجب أن يكون لكل عنصر فعلي صنف قرض مناظر.</span><span class="sxs-lookup"><span data-stu-id="22238-109">Each physical item must have a corresponding loan item.</span></span> <span data-ttu-id="22238-110">يجب أن يصف كل سجل لأصناف القرض ما الصنف الذي يتم إقراضه والشخص المسؤول عن القرض وعدد الأيام التي يمكن إقراض الصنف فيها للعامل.</span><span class="sxs-lookup"><span data-stu-id="22238-110">Each loan item record should describe what is being loaned, who is responsible for the loan, and the number of days the item can loaned to a worker.</span></span> <span data-ttu-id="22238-111">ويمكنك إنشاء أصناف قرض متعددة للأصنف، مثل المفاتيح أو بطاقات الدخول أو الزي الموحد، في نفس الوقت.</span><span class="sxs-lookup"><span data-stu-id="22238-111">You can create multiple loan items, for items such as keys, access cards or uniforms, at the same time.</span></span> 

<span data-ttu-id="22238-112">عند إقراض أحد الأصناف، أدخل تاريخ إقراض الصنف وكذلك تاريخ الإرجاع المخطط.</span><span class="sxs-lookup"><span data-stu-id="22238-112">When loaning an item, enter the date that the item was loaned, and the planned return date.</span></span> <span data-ttu-id="22238-113">وعند إرجاع الصنف، أدخل تاريخ الإرجاع الفعلي.</span><span class="sxs-lookup"><span data-stu-id="22238-113">When the item is returned, enter the actual return date.</span></span>

<span data-ttu-id="22238-114">يمكن للموظفين عرض السجلات الخاصة بالأصناف التي تم إقراضها لهم باستخدام مساحة الخدمة الذاتية للموظف.</span><span class="sxs-lookup"><span data-stu-id="22238-114">Employees can view the records of the items that have been loaned to them using the Employee self-service workspace.</span></span> <span data-ttu-id="22238-115">‏‫كما يمكنهم أيضًا تحرير سجلات موجودة أو إدخال أصناف قرض جديدة، إذا تلقيت أصناف إضافية فعلية.</span><span class="sxs-lookup"><span data-stu-id="22238-115">They can also edit the existing records or enter new loan items, if they've received additional physical items.</span></span>  <span data-ttu-id="22238-116">ويمكن إعداد سير عمل لتوجيه تغييرات لأصناف قرض جديدة أو موجودة من خلال عملية موافقة.‬‏‫</span><span class="sxs-lookup"><span data-stu-id="22238-116">Workflow can be set up to route changes to new or existing loan items through an approval process.</span></span> 

<span data-ttu-id="22238-117">يمكن للمديرين عرض الأصناف المُقرضة لتقاريرهم المباشرة.</span><span class="sxs-lookup"><span data-stu-id="22238-117">Managers can view loaned items for their direct reports.</span></span> <span data-ttu-id="22238-118">كما يمكنهم منح الإذن لإضافة أصناف قرض جديدة بالنيابة عن موظفيهم.</span><span class="sxs-lookup"><span data-stu-id="22238-118">They can also be granted permission to add new loan items on behalf of their employees.</span></span>

 <a name="account-for-lost-or-misplaced-loan-items"></a><span data-ttu-id="22238-119"> الحساب الخاص بأصناف القرض المفقودة أو الموضوعة في غير موضعها</span><span class="sxs-lookup"><span data-stu-id="22238-119">Account for lost or misplaced loan items</span></span>
-----------------------------------------

<span data-ttu-id="22238-120">في حالة تعرض أحد الأصناف للتلف أو تم وضعه في غير موضعه، أدخل سجل إرجاع وهمي.</span><span class="sxs-lookup"><span data-stu-id="22238-120">If an item becomes damaged or misplaced, enter a fictitious return record.</span></span> <span data-ttu-id="22238-121">ثم قم إما بحذف الصنف أو بإبقائه في النظرة العامة وتغيير الوصف للإشارة إلى أن الصنف غير متاح.</span><span class="sxs-lookup"><span data-stu-id="22238-121">Then either delete the item or keep it in the overview and change the description to indicate that the item is not available.</span></span>


<a name="additional-resources"></a><span data-ttu-id="22238-122">الموارد الإضافية</span><span class="sxs-lookup"><span data-stu-id="22238-122">Additional resources</span></span>
--------

[<span data-ttu-id="22238-123">الموارد البشرية</span><span class="sxs-lookup"><span data-stu-id="22238-123">Human resources</span></span>](index.md)


