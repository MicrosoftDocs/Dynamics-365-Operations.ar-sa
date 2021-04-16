---
title: عرض إدخالات الدفاتر اليومية أو الحركات
description: يوضح هذا الإجراء كيفية استخدام استعلام حركات الإيصال للبحث عن إدخالات دفتر اليومية أو الحركات.
author: aprilolson
ms.date: 07/01/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: SysQueryForm, LedgerTransVoucher, LedgerTransBase, Originaldocuments
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: dbeb5af9b14c409347f7f0ac2aeb045929619a3d
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 04/01/2021
ms.locfileid: "5817019"
---
# <a name="view-journal-entries-or-transactions"></a><span data-ttu-id="c6ca3-103">عرض إدخالات الدفاتر اليومية أو الحركات</span><span class="sxs-lookup"><span data-stu-id="c6ca3-103">View journal entries or transactions</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="c6ca3-104">يوضح هذا الإجراء كيفية استخدام استعلام حركات الإيصال للبحث عن إدخالات دفتر اليومية أو الحركات.</span><span class="sxs-lookup"><span data-stu-id="c6ca3-104">This procedure shows how to use the Voucher transactions inquiry to search for journal entries or transactions.</span></span>

1. <span data-ttu-id="c6ca3-105">انتقل إلى **جزء التنقل > الوحدات النمطية > دفتر الأستاذ العام > الاستعلامات والتقارير > حركات الإيصال**‬.</span><span class="sxs-lookup"><span data-stu-id="c6ca3-105">Go to **Navigation pane > Modules > General ledger > Inquiries and reports > Voucher transactions**.</span></span>
2. <span data-ttu-id="c6ca3-106">حدد الحقل الذي ترغب في تحديد معايير تصفية له.</span><span class="sxs-lookup"><span data-stu-id="c6ca3-106">Select the field for which you want to define a filter criteria.</span></span>
3. <span data-ttu-id="c6ca3-107">أدخل معايير التصفية للحقل المحدد.</span><span class="sxs-lookup"><span data-stu-id="c6ca3-107">Enter your filter critieria for the selected field.</span></span> <span data-ttu-id="c6ca3-108">يمكنك إجراء تصفية على قيمة واحدة أو نطاق واحد.</span><span class="sxs-lookup"><span data-stu-id="c6ca3-108">You could filter on a single value or a range.</span></span> <span data-ttu-id="c6ca3-109">عند تعريف نطاق، تأكد من استخدام بناء الجملة الصحيح.</span><span class="sxs-lookup"><span data-stu-id="c6ca3-109">When defining a range, make sure the correct syntax is used.</span></span> <span data-ttu-id="c6ca3-110">يجب أن تكون القيم مفصولة بواسطة نقطة مزدوجة (..).</span><span class="sxs-lookup"><span data-stu-id="c6ca3-110">The values should be separated by a double period (..).</span></span>  
4. <span data-ttu-id="c6ca3-111">انقر فوق علامة التبويب **عمليات الربط‬** لإضافة جداول أخرى لإجراء التصفية منها.</span><span class="sxs-lookup"><span data-stu-id="c6ca3-111">Click the **Joins** tab to add additional tables from which to filter.</span></span>
5. <span data-ttu-id="c6ca3-112">في الشجرة، حدد **الجداول/إدخال دفتر اليومية العام‬**.</span><span class="sxs-lookup"><span data-stu-id="c6ca3-112">In the tree, select **Tables/General journal entry**.</span></span>
6. <span data-ttu-id="c6ca3-113">انقر فوق **إضافة ربط الجدول**.</span><span class="sxs-lookup"><span data-stu-id="c6ca3-113">Click **Add table join**.</span></span>
7. <span data-ttu-id="c6ca3-114">انقر فوق **إلغاء الأمر** إذا قررت عدم إضافة جدول إضافي.</span><span class="sxs-lookup"><span data-stu-id="c6ca3-114">Click **Cancel** if you decide not to add an additional table.</span></span>
8. <span data-ttu-id="c6ca3-115">انقر فوق علامة التبويب **النطاق**.</span><span class="sxs-lookup"><span data-stu-id="c6ca3-115">Click the **Range** tab.</span></span>
9. <span data-ttu-id="c6ca3-116">انقر فوق **موافق** لتشغيل الاستعلام.</span><span class="sxs-lookup"><span data-stu-id="c6ca3-116">Click **OK** to run the query.</span></span>
10. <span data-ttu-id="c6ca3-117">في جزء الإجراءات، انقر فوق **أصل الحركة‬**.</span><span class="sxs-lookup"><span data-stu-id="c6ca3-117">On the Action pane, click **Transaction origin**.</span></span> <span data-ttu-id="c6ca3-118">يمكن استخدام أزرار متعددة حول الشبكة للبحث عن معلومات إضافية حول السجل المحدد للإيصال.</span><span class="sxs-lookup"><span data-stu-id="c6ca3-118">Various buttons about the grid can be used to research additional information about the selected record of the voucher.</span></span> <span data-ttu-id="c6ca3-119">قد لا تكون بعض الأزرار متوفرة، وهذا يتوقف على نوع الحركة والصفات المميزة للحركة.</span><span class="sxs-lookup"><span data-stu-id="c6ca3-119">Some buttons may not be available, depending on the type of transaction and characteristics of the transaction.</span></span>
11. <span data-ttu-id="c6ca3-120">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="c6ca3-120">Close the page.</span></span>
12. <span data-ttu-id="c6ca3-121">في جزء الإجراءات، انقر فوق **المستند الأصلي**.</span><span class="sxs-lookup"><span data-stu-id="c6ca3-121">On the Action pane, Click **Original document**.</span></span>
13. <span data-ttu-id="c6ca3-122">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="c6ca3-122">Close the page.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]