---
title: عكس الإعدادات في دفاتر اليومية والبنود
description: يتناول هذا الموضوع سبب عدم تضمين إدخال عكسي تم إدخاله في دفتر يومية عام في الحركة التي تم ترحيلها.
author: kweekley
ms.date: 04/29/2021
ms.topic: index-page
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2021-5-05
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 74020f6fc9b0fa8e05a1e2a09fd13dcd60490dc0
ms.sourcegitcommit: 817716c2e96f24af0ef1d7d5323afdeccdc602f3
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 05/13/2021
ms.locfileid: "6028546"
---
# <a name="reverse-settings-on-journals-and-lines"></a><span data-ttu-id="00c77-103">عكس الإعدادات في دفاتر اليومية والبنود</span><span class="sxs-lookup"><span data-stu-id="00c77-103">Reverse settings on journals and lines</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="00c77-104">يتناول هذا الموضوع سبب عدم تضمين إدخال عكسي تم إدخاله في دفتر يومية عام في الحركة التي تم ترحيلها.</span><span class="sxs-lookup"><span data-stu-id="00c77-104">This topic addresses why a reversing entry that was entered on a general journal might not be included on the posted transaction.</span></span>  

## <a name="symptom"></a><span data-ttu-id="00c77-105">العَرَضْ</span><span class="sxs-lookup"><span data-stu-id="00c77-105">Symptom</span></span>

<span data-ttu-id="00c77-106">يتضمن دفتر اليومية العام إدخالاً عكسيًا وتاريخًا عكسيًا في دفتر اليومية.</span><span class="sxs-lookup"><span data-stu-id="00c77-106">A general journal includes a reversing entry and reversing date on the journal.</span></span> <span data-ttu-id="00c77-107">عند ترحيل دفتر اليومية، لا يتم عكس أي من الإيصالات.</span><span class="sxs-lookup"><span data-stu-id="00c77-107">When you post the journal, none of the vouchers are reversed.</span></span> <span data-ttu-id="00c77-108">لماذا يحدث هذا؟</span><span class="sxs-lookup"><span data-stu-id="00c77-108">Why does this happen?</span></span>

## <a name="resolution"></a><span data-ttu-id="00c77-109">الحل</span><span class="sxs-lookup"><span data-stu-id="00c77-109">Resolution</span></span>

<span data-ttu-id="00c77-110">عند ترحيل دفتر اليومية، ستظهر عملية العكس فقط في إعدادات **إدخال العكس** و **تاريخ العكس** في قسم **البنود** في الإيصال.</span><span class="sxs-lookup"><span data-stu-id="00c77-110">When the journal is posted, the reversing process looks only at the **Revering entry** and **Reversing date** settings on the **Lines** section of the voucher.</span></span> <span data-ttu-id="00c77-111">يتيح هذا النهج لدفتر اليومية تضمين بعض الإيصالات التي تم وضع علامة عليها للعكس، وأخرى ليست كذلك.</span><span class="sxs-lookup"><span data-stu-id="00c77-111">This approach allows a journal to include some vouchers that are marked for reversing, and others that are not.</span></span>

<span data-ttu-id="00c77-112">يتم استخدام القيم من دفتر اليومية فقط كإعدادات افتراضية عند إضافة بنود *جديدة*.</span><span class="sxs-lookup"><span data-stu-id="00c77-112">The values from the journal are only used as defaults when adding *new* lines.</span></span> <span data-ttu-id="00c77-113">لا يؤثر تغيير القيم في دفتر اليومية على البنود الموجودة.</span><span class="sxs-lookup"><span data-stu-id="00c77-113">Changing the values on the journal doesn’t affect existing lines.</span></span> <span data-ttu-id="00c77-114">في هذا المثال، تم إدخال بنود الإيصال أولاً.</span><span class="sxs-lookup"><span data-stu-id="00c77-114">In this example, the voucher lines were entered first.</span></span> <span data-ttu-id="00c77-115">عند إدخال تفاصيل البند قبل تعيين دفتر اليومية كعكس، فلن يتم تطبيق التعيين كإدخال عكس وتاريخ على أي بنود موجودة.</span><span class="sxs-lookup"><span data-stu-id="00c77-115">When you enter the line detail before designating the journal as reversing, the designation as a reversing entry and date won't be applied to any existing lines.</span></span>

<span data-ttu-id="00c77-116">يؤدي تغيير إدخال العكس أو تاريخ العكس على بند موجود إلى نشر هذا التغيير إلى بنود أخرى في نفس الإيصال.</span><span class="sxs-lookup"><span data-stu-id="00c77-116">Changing the reversing entry or reversing date on an existing line propagates that change to other lines in the same voucher.</span></span> <span data-ttu-id="00c77-117">لتحسين الأداء، لا يتم تحديث الشبكة بعد نشر التغييرات للبنود الأخرى.</span><span class="sxs-lookup"><span data-stu-id="00c77-117">To optimize performance, the grid is not refreshed after propagating changes to other Lines.</span></span> <span data-ttu-id="00c77-118">يمكنك عرض القيم التي تم تحديثها عن طريق تحديث الشبكة.</span><span class="sxs-lookup"><span data-stu-id="00c77-118">You can display the updated values by refreshing the grid.</span></span>


