---
title: عرض إدخالات الدفاتر اليومية أو الحركات
description: يوضح هذا الإجراء كيفية استخدام استعلام حركات الإيصال للبحث عن إدخالات دفتر اليومية أو الحركات.
author: aprilolson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SysQueryForm, LedgerTransVoucher, LedgerTransBase, Originaldocuments
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: c93b581e22665b27c1b99503cc91c20ead14ac81
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 08/01/2019
ms.locfileid: "1834674"
---
# <a name="view-journal-entries-or-transactions"></a><span data-ttu-id="bab1d-103">عرض إدخالات الدفاتر اليومية أو الحركات</span><span class="sxs-lookup"><span data-stu-id="bab1d-103">View journal entries or transactions</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="bab1d-104">يوضح هذا الإجراء كيفية استخدام استعلام حركات الإيصال للبحث عن إدخالات دفتر اليومية أو الحركات.</span><span class="sxs-lookup"><span data-stu-id="bab1d-104">This procedure shows how to use the Voucher transactions inquiry to search for journal entries or transactions.</span></span>

1. <span data-ttu-id="bab1d-105">انتقل إلى دفتر الأستاذ العام > الاستعلامات والتقارير > حركات الإيصال‬.</span><span class="sxs-lookup"><span data-stu-id="bab1d-105">Go to General ledger > Inquiries and reports > Voucher transactions.</span></span>
2. <span data-ttu-id="bab1d-106">حدد الحقل الذي ترغب في تحديد معايير تصفية له.</span><span class="sxs-lookup"><span data-stu-id="bab1d-106">Select the field for which you want to define a filter criteria.</span></span>
3. <span data-ttu-id="bab1d-107">أدخل معايير التصفية للحقل المحدد.</span><span class="sxs-lookup"><span data-stu-id="bab1d-107">Enter your filter critieria for the selected field.</span></span>
    * <span data-ttu-id="bab1d-108">يمكنك إجراء تصفية على قيمة واحدة أو نطاق واحد.</span><span class="sxs-lookup"><span data-stu-id="bab1d-108">You could filter on a single value or a range.</span></span> <span data-ttu-id="bab1d-109">عند تعريف نطاق، تأكد من استخدام بناء الجملة الصحيح.</span><span class="sxs-lookup"><span data-stu-id="bab1d-109">When defining a range, make sure the correct syntax is used.</span></span> <span data-ttu-id="bab1d-110">يجب أن تكون القيم مفصولة بواسطة نقطة مزدوجة (..).</span><span class="sxs-lookup"><span data-stu-id="bab1d-110">The values should be separated by a double period (..).</span></span>  
4. <span data-ttu-id="bab1d-111">انقر فوق علامة التبويب "عمليات الربط‬" لإضافة جداول أخرى لإجراء التصفية منها.</span><span class="sxs-lookup"><span data-stu-id="bab1d-111">Click the Joins tab to add additional tables from which to filter.</span></span>
5. <span data-ttu-id="bab1d-112">في الشجرة، حدد "Tables\General journal entry".</span><span class="sxs-lookup"><span data-stu-id="bab1d-112">In the tree, select 'Tables\General journal entry'.</span></span>
6. <span data-ttu-id="bab1d-113">انقر فوق "‏‫إضافة ربط الجدول‬".</span><span class="sxs-lookup"><span data-stu-id="bab1d-113">Click Add table join.</span></span>
7. <span data-ttu-id="bab1d-114">انقر فوق "إلغاء الأمر" إذا قررت عدم إضافة جدول إضافي.</span><span class="sxs-lookup"><span data-stu-id="bab1d-114">Click Cancel if you decide not to add an additional table.</span></span>
8. <span data-ttu-id="bab1d-115">انقر فوق علامة التبويب "النطاق".</span><span class="sxs-lookup"><span data-stu-id="bab1d-115">Click the Range tab.</span></span>
9. <span data-ttu-id="bab1d-116">انقر فوق موافق لتشغيل الاستعلام.</span><span class="sxs-lookup"><span data-stu-id="bab1d-116">Click OK to run the query.</span></span>
10. <span data-ttu-id="bab1d-117">انقر فوق "أصل الحركة".</span><span class="sxs-lookup"><span data-stu-id="bab1d-117">Click Transaction origin.</span></span>
    * <span data-ttu-id="bab1d-118">يمكن استخدام أزرار متعددة حول الشبكة للبحث عن معلومات إضافية حول السجل المحدد للإيصال.</span><span class="sxs-lookup"><span data-stu-id="bab1d-118">Various buttons about the grid can be used to research additional information about the selected record of the voucher.</span></span> <span data-ttu-id="bab1d-119">قد لا تكون بعض الأزرار متوفرة، وهذا يتوقف على نوع الحركة والصفات المميزة للحركة.</span><span class="sxs-lookup"><span data-stu-id="bab1d-119">Some buttons may not be available, depending on the type of transaction and characteristics of the transaction.</span></span>  
11. <span data-ttu-id="bab1d-120">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="bab1d-120">Close the page.</span></span>
12. <span data-ttu-id="bab1d-121">انقر فوق مستند أصلي.</span><span class="sxs-lookup"><span data-stu-id="bab1d-121">Click Original document.</span></span>
13. <span data-ttu-id="bab1d-122">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="bab1d-122">Close the page.</span></span>

