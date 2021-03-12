---
title: إنشاء مجموعة عقد الإيجار
description: يصف هذا الموضوع كيفية إعداد مجموعات عقد الإيجار. مجموعات عقد الإيجار مطلوبة لإنشاء عقود إيجار جديدة.
author: moaamer
manager: Ann Beebe
ms.date: 10/28/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TaxTable
audience: Application User
ms.reviewer: roschlom
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2020-10-28
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 2c06f6f943c8a47fbe650a67017b95d799914a0e
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 01/15/2021
ms.locfileid: "4971343"
---
# <a name="create-a-lease-group"></a><span data-ttu-id="81936-104">إنشاء مجموعة عقد الإيجار</span><span class="sxs-lookup"><span data-stu-id="81936-104">Create a lease group</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="81936-105">يصف هذا الموضوع كيفية إعداد مجموعات عقد الإيجار.</span><span class="sxs-lookup"><span data-stu-id="81936-105">This topic explains how to set up lease groups.</span></span> <span data-ttu-id="81936-106">مجموعات عقد الإيجار مطلوبة لإنشاء عقود إيجار جديدة.</span><span class="sxs-lookup"><span data-stu-id="81936-106">Lease groups are required to create new leases.</span></span> <span data-ttu-id="81936-107">تقترن دفاتر عقود الإيجار بكل مجموعة عقد إيجار.</span><span class="sxs-lookup"><span data-stu-id="81936-107">Lease books are associated with each lease group.</span></span> <span data-ttu-id="81936-108">تقوم دفاتر عقود الإيجار بتحديد الدفاتر الافتراضية التي يجب إنشاؤها لكل عقد إيجار.</span><span class="sxs-lookup"><span data-stu-id="81936-108">Lease books determine the default books that must be created for each lease.</span></span> <span data-ttu-id="81936-109">يمكنك تعيين حسابات محددة لمجموعة عقد إيجار في الصفحة **معلمات ترحيل عقد الإيجار**.</span><span class="sxs-lookup"><span data-stu-id="81936-109">You can assign specific accounts to a lease group on the **Lease posting parameters** page.</span></span>

## <a name="create-a-lease-book-and-add-a-lease-group"></a><span data-ttu-id="81936-110">إنشاء دفتر عقد إيجار وإضافة مجموعة عقد إيجار</span><span class="sxs-lookup"><span data-stu-id="81936-110">Create a lease book and add a lease group</span></span>

1. <span data-ttu-id="81936-111">انتقل إلى **تأجير الأصول \> الضبط \> مجموعات عقود الإيجار**.</span><span class="sxs-lookup"><span data-stu-id="81936-111">Go to **Asset leasing \> Setup \> Lease groups**.</span></span>
2. <span data-ttu-id="81936-112">في جزء الإجراءات، حدد **جديد** لإضافة مجموعة عقد إيجار.</span><span class="sxs-lookup"><span data-stu-id="81936-112">On the Action Pane, select **New** to add a lease group.</span></span> <span data-ttu-id="81936-113">تتم إضافة بند إلى الشبكة.</span><span class="sxs-lookup"><span data-stu-id="81936-113">A line is added to the grid.</span></span>
3. <span data-ttu-id="81936-114">في البند الجديد، في الحقل **مجموعة عقد الإيجار**، أدخل قيمة.</span><span class="sxs-lookup"><span data-stu-id="81936-114">On the new line, in the **Lease group** field, enter a value.</span></span>
4. <span data-ttu-id="81936-115">في حقل **الوصف**، أدخل قيمة.</span><span class="sxs-lookup"><span data-stu-id="81936-115">In the **Description** field, enter a value.</span></span>

<span data-ttu-id="81936-116">تتم إضافة المعلومات التي قمت بإدخالها للتو إلى الحقل **مجموعة عقد الإيجار** في الصفحة **إضافة عقد إيجار**.</span><span class="sxs-lookup"><span data-stu-id="81936-116">The information that you just entered is added to the **Lease group** field on the **Add lease** page.</span></span>

## <a name="associate-a-book-with-a-lease-group"></a><span data-ttu-id="81936-117">إقران دفتر بمجموعة عقد إيجار</span><span class="sxs-lookup"><span data-stu-id="81936-117">Associate a book with a lease group</span></span>

<span data-ttu-id="81936-118">بعد إنشاء مجموعات عقود الإيجار، يمكنك تعيين دفاتر لكل مجموعة.</span><span class="sxs-lookup"><span data-stu-id="81936-118">After you create lease groups, you can assign books to each group.</span></span> <span data-ttu-id="81936-119">عند إنشاء عقد إيجار وتعيينه لمجموعة عقد إيجار، يقوم النظام بإنشاء مجموعة من الجداول لكل دفتر مقترن بمجموعة عقد الإيجار هذه.</span><span class="sxs-lookup"><span data-stu-id="81936-119">When you create a lease and assign it to a lease group, the system creates a set of schedules for each book that is associated with that lease group.</span></span>

> [!NOTE]
> <span data-ttu-id="81936-120">يجب إعداد الدفاتر قبل تعيينها إلى مجموعة عقد إيجار.</span><span class="sxs-lookup"><span data-stu-id="81936-120">Books must be set up before they can be assigned to a lease group.</span></span>

1. <span data-ttu-id="81936-121">انتقل إلى **تأجير الأصول \> الضبط \> مجموعة عقد الإيجار**.</span><span class="sxs-lookup"><span data-stu-id="81936-121">Go to **Asset leasing \> Setup \> Lease group**.</span></span>
2. <span data-ttu-id="81936-122">حدد مجموعة عقد الإيجار، ثم حدد **الدفاتر**.</span><span class="sxs-lookup"><span data-stu-id="81936-122">Select a lease group, and then select **Books**.</span></span>
3. <span data-ttu-id="81936-123">حدد **جديد**، ثم في الحقل **نوع الدفتر**، حدد الدفتر الذي تريد تعيينه لمجموعة عقد الإيجار.</span><span class="sxs-lookup"><span data-stu-id="81936-123">Select **New**, and then, in the **Book type** field, select the book to assign to the lease group.</span></span> <span data-ttu-id="81936-124">يمكنك تعيين عدة دفاتر لمجموعة عقد إيجار إذا كان من الضروري حساب عقد إيجار لكل منها بطرق مختلفة.</span><span class="sxs-lookup"><span data-stu-id="81936-124">You can assign multiple books to a lease group if a lease must be accounted for in different ways.</span></span>
