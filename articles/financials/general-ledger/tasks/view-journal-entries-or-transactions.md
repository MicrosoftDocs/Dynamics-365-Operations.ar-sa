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
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 53e966a4caf6ee8907b05b5fd9c0978187d64f1d
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 01/29/2019
ms.locfileid: "349252"
---
# <a name="view-journal-entries-or-transactions"></a><span data-ttu-id="318a4-103">عرض إدخالات الدفاتر اليومية أو الحركات</span><span class="sxs-lookup"><span data-stu-id="318a4-103">View journal entries or transactions</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="318a4-104">يوضح هذا الإجراء كيفية استخدام استعلام حركات الإيصال للبحث عن إدخالات دفتر اليومية أو الحركات.</span><span class="sxs-lookup"><span data-stu-id="318a4-104">This procedure shows how to use the Voucher transactions inquiry to search for journal entries or transactions.</span></span>

1. <span data-ttu-id="318a4-105">انتقل إلى دفتر الأستاذ العام > الاستعلامات والتقارير > حركات الإيصال‬.</span><span class="sxs-lookup"><span data-stu-id="318a4-105">Go to General ledger > Inquiries and reports > Voucher transactions.</span></span>
2. <span data-ttu-id="318a4-106">حدد الحقل الذي ترغب في تحديد معايير تصفية له.</span><span class="sxs-lookup"><span data-stu-id="318a4-106">Select the field for which you want to define a filter criteria.</span></span>
3. <span data-ttu-id="318a4-107">أدخل معايير التصفية للحقل المحدد.</span><span class="sxs-lookup"><span data-stu-id="318a4-107">Enter your filter critieria for the selected field.</span></span>
    * <span data-ttu-id="318a4-108">يمكنك إجراء تصفية على قيمة واحدة أو نطاق واحد.</span><span class="sxs-lookup"><span data-stu-id="318a4-108">You could filter on a single value or a range.</span></span> <span data-ttu-id="318a4-109">عند تعريف نطاق، تأكد من استخدام بناء الجملة الصحيح.</span><span class="sxs-lookup"><span data-stu-id="318a4-109">When defining a range, make sure the correct syntax is used.</span></span> <span data-ttu-id="318a4-110">يجب أن تكون القيم مفصولة بواسطة نقطة مزدوجة (..).</span><span class="sxs-lookup"><span data-stu-id="318a4-110">The values should be separated by a double period (..).</span></span>  
4. <span data-ttu-id="318a4-111">انقر فوق علامة التبويب "عمليات الربط‬" لإضافة جداول أخرى لإجراء التصفية منها.</span><span class="sxs-lookup"><span data-stu-id="318a4-111">Click the Joins tab to add additional tables from which to filter.</span></span>
5. <span data-ttu-id="318a4-112">في الشجرة، حدد "Tables\General journal entry".</span><span class="sxs-lookup"><span data-stu-id="318a4-112">In the tree, select 'Tables\General journal entry'.</span></span>
6. <span data-ttu-id="318a4-113">انقر فوق "‏‫إضافة ربط الجدول‬".</span><span class="sxs-lookup"><span data-stu-id="318a4-113">Click Add table join.</span></span>
7. <span data-ttu-id="318a4-114">انقر فوق "إلغاء الأمر" إذا قررت عدم إضافة جدول إضافي.</span><span class="sxs-lookup"><span data-stu-id="318a4-114">Click Cancel if you decide not to add an additional table.</span></span>
8. <span data-ttu-id="318a4-115">انقر فوق علامة التبويب "النطاق".</span><span class="sxs-lookup"><span data-stu-id="318a4-115">Click the Range tab.</span></span>
9. <span data-ttu-id="318a4-116">انقر فوق موافق لتشغيل الاستعلام.</span><span class="sxs-lookup"><span data-stu-id="318a4-116">Click OK to run the query.</span></span>
10. <span data-ttu-id="318a4-117">انقر فوق "أصل الحركة".</span><span class="sxs-lookup"><span data-stu-id="318a4-117">Click Transaction origin.</span></span>
    * <span data-ttu-id="318a4-118">يمكن استخدام أزرار متعددة حول الشبكة للبحث عن معلومات إضافية حول السجل المحدد للإيصال.</span><span class="sxs-lookup"><span data-stu-id="318a4-118">Various buttons about the grid can be used to research additional information about the selected record of the voucher.</span></span> <span data-ttu-id="318a4-119">قد لا تكون بعض الأزرار متوفرة، وهذا يتوقف على نوع الحركة والصفات المميزة للحركة.</span><span class="sxs-lookup"><span data-stu-id="318a4-119">Some buttons may not be available, depending on the type of transaction and characteristics of the transaction.</span></span>  
11. <span data-ttu-id="318a4-120">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="318a4-120">Close the page.</span></span>
12. <span data-ttu-id="318a4-121">انقر فوق مستند أصلي.</span><span class="sxs-lookup"><span data-stu-id="318a4-121">Click Original document.</span></span>
13. <span data-ttu-id="318a4-122">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="318a4-122">Close the page.</span></span>

