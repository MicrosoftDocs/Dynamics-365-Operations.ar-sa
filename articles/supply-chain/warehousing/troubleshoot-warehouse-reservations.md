---
title: استكشاف الأخطاء في عمليات الحجز بإدارة المستودعات وإصلاحها
description: يوضح هذا الموضوع كيفية إصلاح المشكلات الشائعة التي قد تواجهها أثناء العمل مع عمليات حجز المستودعات في Microsoft Dynamics 365 Supply Chain Management.
author: perlynne
ms.date: 10/19/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application user
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2020-10-19
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: d0d73396772ed9e8397797d6685fb550d911303b
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 04/01/2021
ms.locfileid: "5828096"
---
# <a name="troubleshoot-reservations-in-warehouse-management"></a><span data-ttu-id="5c049-103">استكشاف الأخطاء في عمليات الحجز بإدارة المستودعات وإصلاحها</span><span class="sxs-lookup"><span data-stu-id="5c049-103">Troubleshoot reservations in warehouse management</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="5c049-104">يوضح هذا الموضوع كيفية إصلاح المشكلات الشائعة التي قد تواجهها أثناء العمل مع عمليات حجز المستودعات في Microsoft Dynamics 365 Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="5c049-104">This topic describes how to fix common issues that you might encounter while you work with warehouse reservations in Microsoft Dynamics 365 Supply Chain Management.</span></span>

<span data-ttu-id="5c049-105">بالنسبة إلى الموضوعات المتعلقة بتسجيلات الدُفعات والرقم التسلسلي، راجع [استكشاف أخطاء دفعة المستودع والتسلسل الهرمي للحجز التسلسلي وإصلاحها](troubleshoot-warehouse-batch-and-serial-reservation-hierarchies.md).</span><span class="sxs-lookup"><span data-stu-id="5c049-105">For topics that are related to batch and serial number registrations, see [Troubleshoot warehouse batch and serial reservation hierarchies](troubleshoot-warehouse-batch-and-serial-reservation-hierarchies.md).</span></span>

## <a name="i-receive-the-following-error-message-reservations-cannot-be-removed-because-there-is-work-created-which-relies-on-the-reservations"></a><span data-ttu-id="5c049-106">أتلقى رسالة الخطأ " لا يمكن إزالة الحجوزات نظرًا لوجود عمل مُنشأ يعتمد على الحجوزات".‬</span><span class="sxs-lookup"><span data-stu-id="5c049-106">I receive the following error message: "Reservations cannot be removed because there is work created which relies on the reservations."</span></span>

### <a name="issue-description"></a><span data-ttu-id="5c049-107">وصف المشكلة</span><span class="sxs-lookup"><span data-stu-id="5c049-107">Issue description</span></span>

<span data-ttu-id="5c049-108">لا يمكنك إلغاء حجز المخزون في بند مبيعات ، نظرا لوجود عمل مفتوح للبند.</span><span class="sxs-lookup"><span data-stu-id="5c049-108">You can't unreserve inventory on a sales line, because there is open work against the line.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="5c049-109">حل المشكلة</span><span class="sxs-lookup"><span data-stu-id="5c049-109">Issue resolution</span></span>

<span data-ttu-id="5c049-110">التحقق من وجود عمل مجموعه التعبئة المفتوحة لإحضار الصنف من محطه تعبئة إلى موقع آخر (مثل *باب الخليج*).</span><span class="sxs-lookup"><span data-stu-id="5c049-110">Investigate whether open packing group work exists to bring the item from a packing station to another location (such as *Baydoor*).</span></span> <span data-ttu-id="5c049-111">قم بمراجعه السجلات الموجودة في الصفحتين **سجل محفوظات إنشاء العمل** و **وتفاصيل العمل** لتحديد ما يقوم بحجز المخزون فعليا ، ثم قم بإكمال العمل أو حذفه لتحرير الحجز.</span><span class="sxs-lookup"><span data-stu-id="5c049-111">Review the records on the **Work creation history log** and **Work details** pages to determine what is physically reserving the inventory, and then complete or delete the work to free up the reservation.</span></span>

## <a name="i-receive-the-following-error-message-inventory-quantity--1-could-not-be-updated-due-to-insufficient-inventory-transactions-for-item-2"></a><span data-ttu-id="5c049-112">أتلقى رسالة الخطا التالية: "تعذر تحديث كميه المخزون- %1 بسبب عدم كفاية حركات المخزون للصنف %2 ...."</span><span class="sxs-lookup"><span data-stu-id="5c049-112">I receive the following error message: "Inventory quantity -%1 could not be updated due to insufficient inventory transactions for item %2...."</span></span>

### <a name="issue-description"></a><span data-ttu-id="5c049-113">وصف المشكلة</span><span class="sxs-lookup"><span data-stu-id="5c049-113">Issue description</span></span>

<span data-ttu-id="5c049-114">قد تحدث هذه المشكلة في حاله عدم تمكن النظام من تحديث كميه مخزون نظرا لعدم وجود حركات مخزون كافيه بالابعاد المحددة.</span><span class="sxs-lookup"><span data-stu-id="5c049-114">This issue can occur if the system can't update an inventory quantity because there aren't enough inventory transactions that have the specified dimensions.</span></span> <span data-ttu-id="5c049-115">فيما يلي نص رسالة الخطأ الكاملة.</span><span class="sxs-lookup"><span data-stu-id="5c049-115">Here is the full text of the full error message:</span></span>

> <span data-ttu-id="5c049-116">تعذر تحديثكميه المخزون - %1 بسبب عدم كفاية حركات المخزون الخاصة بالصنف %2 ذي حجم الابعاد = %3، اللون = %4، الإضافات = %5، الموقع = %6، المستودع = %7، الموقع = %8، حاله المخزون = متاح، لوح الترخيص = %9، رقم المجموعة = %10 لمعرف المرجع %11 في معرف الشحنة %12.</span><span class="sxs-lookup"><span data-stu-id="5c049-116">Inventory quantity -%1 could not be updated due to insufficient inventory transactions for item %2 with dimensions Size=%3, Color=%4, Additions=%5, Site=%6, Warehouse=%7, Location=%8, Inventory status=Available, License plate=%9, Batch number=%10 for reference ID %11 on Lot ID %12.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="5c049-117">حل المشكلة</span><span class="sxs-lookup"><span data-stu-id="5c049-117">Issue resolution</span></span>

<span data-ttu-id="5c049-118">تاكد من عدم قيام إيه حركات مخزون بالفعل بحجز الكمية.</span><span class="sxs-lookup"><span data-stu-id="5c049-118">Make sure that no inventory transactions are physically reserving the quantity.</span></span> <span data-ttu-id="5c049-119">علي سبيل المثال ، قد تقوم هذه الحركات بفتح أوامر الجودة أو سجلات حظر المخزون أو أوامر المخرجات.</span><span class="sxs-lookup"><span data-stu-id="5c049-119">For example, these transactions might open quality orders, inventory blocking records, or output orders.</span></span>

## <a name="i-receive-the-following-error-message-physical-on-handcannot-be-reserved-because-only-000-are-available-in-the-inventory"></a><span data-ttu-id="5c049-120">أتلقى رسالة الخطا التالية: "الفعلي... لا يمكن حجزه لان 0.00 فقط متاح في المخزون. "</span><span class="sxs-lookup"><span data-stu-id="5c049-120">I receive the following error message: "Physical on-hand...cannot be reserved because only 0.00 are available in the inventory."</span></span>

### <a name="issue-description"></a><span data-ttu-id="5c049-121">وصف المشكلة</span><span class="sxs-lookup"><span data-stu-id="5c049-121">Issue description</span></span>

<span data-ttu-id="5c049-122">قد تحدث هذه المشكلة في حاله عدم تمكن النظام من تحديث كميه مخزون نظرا لعدم وجود حركات مخزون كافيه بالابعاد المحددة.</span><span class="sxs-lookup"><span data-stu-id="5c049-122">This issue can occur if the system can't update an inventory quantity because there aren't enough inventory transactions that have the specified dimensions.</span></span> <span data-ttu-id="5c049-123">فيما يلي نص رسالة الخطأ الكاملة.</span><span class="sxs-lookup"><span data-stu-id="5c049-123">Here is the full text of the full error message:</span></span>

> <span data-ttu-id="5c049-124">موقع الفعلي = %1، المستودع = %2، حاله المخزون = متاح، رقم المجموعة = %3، المالك = %4 : لا يمكن حجز %5 نظرا لتوفر 0.00 فقط في المخزون.</span><span class="sxs-lookup"><span data-stu-id="5c049-124">Physical on-hand Site=%1, Warehouse=%2, Inventory status=Available, Batch number=%3, Owner=%4: %5 cannot be reserved because only 0.00 are available in the inventory.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="5c049-125">حل المشكلة</span><span class="sxs-lookup"><span data-stu-id="5c049-125">Issue resolution</span></span>

<span data-ttu-id="5c049-126">قد يكون سبب هذه المشكلة هو فتح العمل.</span><span class="sxs-lookup"><span data-stu-id="5c049-126">This issue is probably caused by open work.</span></span> <span data-ttu-id="5c049-127">قم اما بإكمال العمل أو الاستلام دون إنشاء العمل.</span><span class="sxs-lookup"><span data-stu-id="5c049-127">Either complete the work or receive without work creation.</span></span> <span data-ttu-id="5c049-128">تاكد من عدم قيام إيه حركات مخزون بالفعل بحجز الكمية.</span><span class="sxs-lookup"><span data-stu-id="5c049-128">Make sure that no inventory transactions are physically reserving the quantity.</span></span> <span data-ttu-id="5c049-129">علي سبيل المثال ، قد تكون هذه الحركات أوامر جودة مفتوحة أو سجلات حظر المخزون أو أوامر المخرجات.</span><span class="sxs-lookup"><span data-stu-id="5c049-129">For example, these transactions might be open quality orders, inventory blocking records, or output orders.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
