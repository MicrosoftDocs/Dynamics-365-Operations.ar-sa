---
title: إدارة إجازات الغياب
description: ينقلك هذا الإجراء عبر عملية إنشاء سجلات إجازة الموظف.
author: andreabichsel
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: HcmWorker, HcmEmploymentLeave
audience: Application User
ms.reviewer: anbichse
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 61729d384b1a403f14ce1bcf227074aa28ab369a
ms.sourcegitcommit: f5e31c34640add6d40308ac1365cc0ee60e60e24
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 12/08/2020
ms.locfileid: "4693006"
---
# <a name="manage-leave-of-absence"></a><span data-ttu-id="83428-103">إدارة إجازات الغياب</span><span class="sxs-lookup"><span data-stu-id="83428-103">Manage leave of absence</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="83428-104">ينقلك هذا الإجراء عبر عملية إنشاء سجلات إجازة الموظف.</span><span class="sxs-lookup"><span data-stu-id="83428-104">This procedure walks through the creation of employee leave records.</span></span> <span data-ttu-id="83428-105">يمكنك تعقب وقت الإجازة لأسباب تشمل الأنشطة الطبية أو التعليمية أو الأبوية.</span><span class="sxs-lookup"><span data-stu-id="83428-105">You can track leave time for reasons that include medical, educational, or parental activities.</span></span> <span data-ttu-id="83428-106">شركة بيانات العرض التوضيحي التي تم استخدامها لإنشاء هذا الإجراء هي USMF.</span><span class="sxs-lookup"><span data-stu-id="83428-106">The demo data company used to create this procedure is USMF.</span></span>

1. <span data-ttu-id="83428-107">انتقل إلى الموارد البشرية > العاملون > الموظفون.</span><span class="sxs-lookup"><span data-stu-id="83428-107">Go to Human resources > Workers > Employees.</span></span>
2. <span data-ttu-id="83428-108">في القائمة، حدد موظفًا.</span><span class="sxs-lookup"><span data-stu-id="83428-108">In the list, select an employee.</span></span>
3. <span data-ttu-id="83428-109">اعرض معلومات مفصلة للموظف المحدد عن طريق تحديد اسم الموظف.</span><span class="sxs-lookup"><span data-stu-id="83428-109">Display detailed information for the selected employee by selecting the employee's name.</span></span>
4. <span data-ttu-id="83428-110">انقر فوق علامة التبويب "التوظيف‬‬".</span><span class="sxs-lookup"><span data-stu-id="83428-110">Click the Employment tab.</span></span>
5. <span data-ttu-id="83428-111">انقر فوق "إجازة".</span><span class="sxs-lookup"><span data-stu-id="83428-111">Click Leave.</span></span>
6. <span data-ttu-id="83428-112">انقر فوق "جديد".</span><span class="sxs-lookup"><span data-stu-id="83428-112">Click New.</span></span>
7. <span data-ttu-id="83428-113">في الحقل "نوع الإجازة"، انقر فوق زر القائمة المنسدلة لفتح البحث.</span><span class="sxs-lookup"><span data-stu-id="83428-113">In the Leave type field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="83428-114">يمكنك إقران نوع إجازة مع كود الأرباح في النموذج "أنواع الإجازات".</span><span class="sxs-lookup"><span data-stu-id="83428-114">You can associate a leave type to an earning code in the Leave types form.</span></span> <span data-ttu-id="83428-115">إذا كان نوع الإجازة مقترنًا مع كود الأرباح، فسيتم إنشاء بند أرباح مع كود الأرباح المقترن أثناء فترة الإجازة التي تقوم بإدخالها.</span><span class="sxs-lookup"><span data-stu-id="83428-115">If a leave type is associated with an earning code, an earning line will be generated with the associated earning code during the leave period that you enter.</span></span>  
8. <span data-ttu-id="83428-116">في القائمة، حدد نوع إجازة.</span><span class="sxs-lookup"><span data-stu-id="83428-116">In the list, select a leave type.</span></span> 
    * <span data-ttu-id="83428-117">على سبيل المثال: التبني</span><span class="sxs-lookup"><span data-stu-id="83428-117">For example: Adoption</span></span>  
9. <span data-ttu-id="83428-118">أدخل تاريخ بدء الإجازة.</span><span class="sxs-lookup"><span data-stu-id="83428-118">Enter the date that the leave will start.</span></span> <span data-ttu-id="83428-119">على سبيل المثال: "2015-10-26"</span><span class="sxs-lookup"><span data-stu-id="83428-119">Example: '2015-10-26'</span></span>
    * <span data-ttu-id="83428-120">على سبيل المثال: 2015-10-26</span><span class="sxs-lookup"><span data-stu-id="83428-120">For example:  2015-10-26</span></span>  
10. <span data-ttu-id="83428-121">أدخل تاريخ بدء الإجازة.</span><span class="sxs-lookup"><span data-stu-id="83428-121">Enter the date that the leave will start.</span></span> 
    * <span data-ttu-id="83428-122">على سبيل المثال: 2015-11-20</span><span class="sxs-lookup"><span data-stu-id="83428-122">For example:  2015-11-20</span></span>  
11. <span data-ttu-id="83428-123">في حقل "الإشعار"، أدخل وصفًا.</span><span class="sxs-lookup"><span data-stu-id="83428-123">In the note field, enter a description.</span></span>
    * <span data-ttu-id="83428-124">على سبيل المثال: إجازة للتبني</span><span class="sxs-lookup"><span data-stu-id="83428-124">For example: Leave for adoption</span></span>  
12. <span data-ttu-id="83428-125">انقر فوق "حفظ".</span><span class="sxs-lookup"><span data-stu-id="83428-125">Click Save.</span></span>

