---
title: ترحيل إدخالات دفتر يومية تسوية الانتقال في تأجير الأصول
description: يصف هذا الموضوع الوظيفة التي تتيح لك إمكانية نقل حافظة الإيجار إلى مقاييس محاسبة الإيجار الجديدة، وموضوع صياغة مقاييس المحاسبة 842 (ASC 842) ومقياس Financial Reporting الدولي 16 (IFRS 16).
author: moaamer
ms.date: 10/28/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2020-10-28
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: ea61a0d6e30695a2ef6b93529fcf3d21882c9cd2
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 04/01/2021
ms.locfileid: "5819760"
---
# <a name="post-transition-adjustment-journal-entries-in-asset-leasing"></a><span data-ttu-id="dcfcf-103">ترحيل إدخالات دفتر يومية تسوية الانتقال في تأجير الأصول</span><span class="sxs-lookup"><span data-stu-id="dcfcf-103">Post transition adjustment journal entries in Asset leasing</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="dcfcf-104">يصف هذا الموضوع الوظيفة التي تتيح لك إمكانية نقل حافظة الإيجار إلى مقاييس محاسبة الإيجار الجديدة: موضوع صياغة مقاييس المحاسبة 842 (ASC 842)، وهو المقياس في مبادئ المحاسبة المقبولة بشكل عام في الولايات المتحدة (US GAAP) ومقاييس Financial Reporting الدولية 16 (IFRS 16).</span><span class="sxs-lookup"><span data-stu-id="dcfcf-104">This topic describes the functionality that lets you transition a lease portfolio to the new lease accounting standards: Accounting Standards Codification Topic 842 (ASC 842), which is the standard in Generally Accepted Accounting Principles in the US (US GAAP), and International Financial Reporting Standard 16 (IFRS 16).</span></span>

<span data-ttu-id="dcfcf-105">للحصول على معلومات حول كيفية إعداد دفتر الانتقال إلى المقاييس الجديدة، راجع [إعداد دفاتر الإيجار](set-up-lease-books.md).</span><span class="sxs-lookup"><span data-stu-id="dcfcf-105">For information about how to set up a book for the transition to the new standards, see [Set up lease books](set-up-lease-books.md).</span></span>

<span data-ttu-id="dcfcf-106">عند إنشاء إدخال دفتر يومية تسوية الانتقال، فإنه يتم إنشاء إدخال دفتر اليومية.</span><span class="sxs-lookup"><span data-stu-id="dcfcf-106">When you create a transition adjustment journal entry, a journal entry is generated.</span></span> <span data-ttu-id="dcfcf-107">يعكس هذا الإدخال تأثير الميزانية العمومية لتسجيل عقد الإيجار ضمن المقاييس الجديدة في ذلك التاريخ.</span><span class="sxs-lookup"><span data-stu-id="dcfcf-107">This entry reflects the balance sheet impact of recording the lease under the new standards on that date.</span></span> <span data-ttu-id="dcfcf-108">يتم خصم حساب الأصل المناسب لمبلغ الحمل في ذلك التاريخ، وتتم إضافة حساب الالتزام.</span><span class="sxs-lookup"><span data-stu-id="dcfcf-108">The appropriate asset account is debited for the carrying amount on that date, and the liability account is credited.</span></span> <span data-ttu-id="dcfcf-109">إما أن يكون الفرق مدينًا أو دائنًا بالأرباح المحتجزة.</span><span class="sxs-lookup"><span data-stu-id="dcfcf-109">The difference is either debited or credited to retained earnings.</span></span>

<span data-ttu-id="dcfcf-110">لترحيل تسوية الانتقال في التوافق مع المقاييس المحاسبية الجديدة، اتبع الخطوات التالية.</span><span class="sxs-lookup"><span data-stu-id="dcfcf-110">To post a transition adjustment in compliance with the new accounting standards, follow these steps.</span></span>

1. <span data-ttu-id="dcfcf-111">في الصفحة **ملخص عقد الإيجار**، حدد عقد الإيجار، ثم حدد **الدفاتر**.</span><span class="sxs-lookup"><span data-stu-id="dcfcf-111">On the **Lease summary** page, select the lease, and then select **Books**.</span></span>
2. <span data-ttu-id="dcfcf-112">في الدفتر، حدد **جدول الدفع**.</span><span class="sxs-lookup"><span data-stu-id="dcfcf-112">In the book, select **Payment schedule**.</span></span>
3. <span data-ttu-id="dcfcf-113">في مربع الحوار **جدول الدفع**، حدد **تأكيد**.</span><span class="sxs-lookup"><span data-stu-id="dcfcf-113">In the **Payment schedule** dialog box, select **Confirm**.</span></span> <span data-ttu-id="dcfcf-114">ثم أغلق مربع الحوار.</span><span class="sxs-lookup"><span data-stu-id="dcfcf-114">Then close the dialog box.</span></span>
4. <span data-ttu-id="dcfcf-115">حدد **تسوية الانتقال**.</span><span class="sxs-lookup"><span data-stu-id="dcfcf-115">Select **Transition adjustment**.</span></span>

    > [!NOTE]
    > <span data-ttu-id="dcfcf-116">لا يمكن إنشاء تسوية انتقال إلا لدفاتر الإيجار التي يتم تعيينها إلى دفتر الذي يكون به الحقل **دفتر الانتقال** متوفرًا.</span><span class="sxs-lookup"><span data-stu-id="dcfcf-116">A transition adjustment can be created only for lease books that are assigned to a book where the **Transition book** field is available.</span></span> <span data-ttu-id="dcfcf-117">إذا كانت القيمة الموجودة في الحقل **بدء الإيجار** متأخرة عن تاريخ الانتقال، فلن يتم تحديث القيمة الموجودة في الحقل **تسوية الانتقال**.</span><span class="sxs-lookup"><span data-stu-id="dcfcf-117">If the value in the **Lease commencement** field is later than the transition date, the value in the **Transition adjustment** field won't be updated.</span></span>

5. <span data-ttu-id="dcfcf-118">لعرض إدخال دفتر اليومية، حدد **دفاتر يومية تأجير الأصول**.</span><span class="sxs-lookup"><span data-stu-id="dcfcf-118">To view the journal entry, select **Asset leasing journals**.</span></span>
6. <span data-ttu-id="dcfcf-119">حدد دفتر اليومية الجديد، ثم حدد **ترحيل**.</span><span class="sxs-lookup"><span data-stu-id="dcfcf-119">Select the new journal, and then select **Post**.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]