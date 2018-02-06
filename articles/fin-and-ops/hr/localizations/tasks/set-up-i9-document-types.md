--- 
title: "إعداد أنواع المستندات I-9"
description: "يوضح هذا الإجراء كيفية عرض وإعداد أنواع المستندات التي يتم استخدامها للتحقق من نموذج I-9."
author: ShielaSogge
manager: AnnBe
ms.date: 11/01/2017
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: rschloma
ms.search.scope: Operations, Talent
ms.search.region: Global
ms.author: shielas
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: a05fec7b79003d5b98470d85644d70bd1dbac285
ms.openlocfilehash: d3d2f38327ea82ecddf998161edf86bf32e04db0
ms.contentlocale: ar-sa
ms.lasthandoff: 02/06/2018

---
# <a name="set-up-i-9-document-types"></a><span data-ttu-id="82d81-103">إعداد أنواع المستندات I-9</span><span class="sxs-lookup"><span data-stu-id="82d81-103">Set up I-9 document types</span></span>

[!include[task guide banner](../../../includes/task-guide-banner.md)]

<span data-ttu-id="82d81-104">يوضح هذا الإجراء كيفية عرض وإعداد أنواع المستندات التي يتم استخدامها للتحقق من نموذج I-9.</span><span class="sxs-lookup"><span data-stu-id="82d81-104">This procedure shows how to view and set up document types that are used for I-9 verification.</span></span> <span data-ttu-id="82d81-105">قبل إعداد أنواع مستندات I-9، يجب أيضًا تعيين وكالات الإصدار وأنواع التعريف.</span><span class="sxs-lookup"><span data-stu-id="82d81-105">Before you set up I-9 document types, you must also set up the issuing agencies and identification types.</span></span> <span data-ttu-id="82d81-106">شركة بيانات العرض التوضيحي المستخدمة لإنشاء هذا الإجراء هي USMF، وتتضمن أمثلة عن وكالات الإصدار وأنواع التعريفات المطلوبة لإكمال العملية.</span><span class="sxs-lookup"><span data-stu-id="82d81-106">The demo data company used to create this procedure is USMF, which includes examples of the issue agencies and identification types that are needed to complete the procedure.</span></span>

1. <span data-ttu-id="82d81-107">انتقل إلى الموارد البشرية > العاملون > I-9 > أنواع المستندات I-9‬.</span><span class="sxs-lookup"><span data-stu-id="82d81-107">Go to Human resources > Workers > I-9 > I-9 document types.</span></span>
2. <span data-ttu-id="82d81-108">انقر فوق "جديد".</span><span class="sxs-lookup"><span data-stu-id="82d81-108">Click New.</span></span>
3. <span data-ttu-id="82d81-109">في حقل "نوع المستند I-9‬"، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="82d81-109">In the I-9 document type field, type a value.</span></span>
    * <span data-ttu-id="82d81-110">على سبيل المثال: معرف المدرسة</span><span class="sxs-lookup"><span data-stu-id="82d81-110">Example: School ID.</span></span>  
4. <span data-ttu-id="82d81-111">تحديد نوع التعريف.</span><span class="sxs-lookup"><span data-stu-id="82d81-111">Select the identification type.</span></span>  <span data-ttu-id="82d81-112">على سبيل المثال: معرف المدرسة</span><span class="sxs-lookup"><span data-stu-id="82d81-112">Example:  School ID</span></span>
    * <span data-ttu-id="82d81-113">تتضمن أمثلة أنواع التعريف رقم التأمين الاجتماعي (SSN) أو رقم التأشيرة أو معرف جواز السفر أو رخصة القيادة.</span><span class="sxs-lookup"><span data-stu-id="82d81-113">Examples of identification types include a Social Security number (SSN), visa number, passport ID, or driver's license.</span></span>  
5. <span data-ttu-id="82d81-114">حدد قائمة المستندات I-9 المستخدمة لنوع المستند.</span><span class="sxs-lookup"><span data-stu-id="82d81-114">Select the I-9 document list that is used for the document type.</span></span>
    * <span data-ttu-id="82d81-115">كجزء من عملية I-9، يجب على الموظفين تقديم وثائق توضح لرب العمل هويتهم وتصريح العمل‬ الخاص بهم.</span><span class="sxs-lookup"><span data-stu-id="82d81-115">As part of the I-9 process, employees must present documentation that shows the employer their identity and employment authorization.</span></span> <span data-ttu-id="82d81-116">يتضمن موقع خدمات الهجرة والمواطنة في الولايات المتحدة معلومات حول المستندات المقبولة، والقائمة التي تنتمي إليها.</span><span class="sxs-lookup"><span data-stu-id="82d81-116">The US Citizenship and Immigration Services website contains information about which documents are acceptable, and which list they belong to.</span></span>  <span data-ttu-id="82d81-117">http://www.uscis.gov</span><span class="sxs-lookup"><span data-stu-id="82d81-117">http://www.uscis.gov</span></span>  
6. <span data-ttu-id="82d81-118">في الحقل "النموذج"، أدخل رقم النموذج الرسمي لنوع المستند.</span><span class="sxs-lookup"><span data-stu-id="82d81-118">In the Form field, Enter the official form number for the document type.</span></span> <span data-ttu-id="82d81-119">على سبيل المثال: معرف المدرسة</span><span class="sxs-lookup"><span data-stu-id="82d81-119">Example: School ID.</span></span>
    * <span data-ttu-id="82d81-120">يمكن العثور على أرقام النموذج الرسمي على موقع خدمات الهجرة والمواطنة الأمريكية.</span><span class="sxs-lookup"><span data-stu-id="82d81-120">The official form numbers can be found on the US Citizenship and Immigration Services website.</span></span>  <span data-ttu-id="82d81-121">http://www.uscis.gov</span><span class="sxs-lookup"><span data-stu-id="82d81-121">http://www.uscis.gov</span></span>  
7. <span data-ttu-id="82d81-122">حدد خانة الاختيار "نشط" أو قم إلغاء تحديدها.</span><span class="sxs-lookup"><span data-stu-id="82d81-122">Check or uncheck the Active checkbox.</span></span>
8. <span data-ttu-id="82d81-123">في الحقل "انتهاء الصلاحية"، قم بتعيين التاريخ إلى ''2019-10-27".</span><span class="sxs-lookup"><span data-stu-id="82d81-123">In the Expire field, set the date to '2019-10-27'.</span></span>
    * <span data-ttu-id="82d81-124">تاريخ انتهاء الصلاحية اختياري.</span><span class="sxs-lookup"><span data-stu-id="82d81-124">The expiration date is optional.</span></span>  
9. <span data-ttu-id="82d81-125">حدد الوكالة التي أصدرت نوع المستند.</span><span class="sxs-lookup"><span data-stu-id="82d81-125">Select the agency that issued the document type.</span></span> <span data-ttu-id="82d81-126">على سبيل المثال: المقاطعة/المنطقة</span><span class="sxs-lookup"><span data-stu-id="82d81-126">Example: Province/territory</span></span>
10. <span data-ttu-id="82d81-127">انقر فوق "حفظ".</span><span class="sxs-lookup"><span data-stu-id="82d81-127">Click Save.</span></span>


