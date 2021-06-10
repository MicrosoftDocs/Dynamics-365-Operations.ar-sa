---
title: تمت مطالبتك بحفظ إعدادات تغطية الصنف حتى إذا لم تقم بأية تغييرات
description: تمت مطالبتك بحفظ إعدادات تغطية الصنف حتى إذا لم تقم بأية تغييرات.
author: ChristianRytt
ms.date: 4/11/2021
ms.topic: troubleshooting
ms.search.form: DataManagementWorkspace_
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: angarmas
ms.search.validFrom: 2021-04-11
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: 3dfa974740420433af1e1b37630b22509510c91b
ms.sourcegitcommit: 3c15a26e9708adc9a75082dc551f0a3a0a7d89f4
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 05/17/2021
ms.locfileid: "6049450"
---
# <a name="youre-prompted-to-save-item-coverage-settings-even-though-you-made-no-changes"></a><span data-ttu-id="88bbe-103">تمت مطالبتك بحفظ إعدادات تغطية الصنف حتى إذا لم تقم بأية تغييرات</span><span class="sxs-lookup"><span data-stu-id="88bbe-103">You're prompted to save item coverage settings even though you made no changes</span></span>

<span data-ttu-id="88bbe-104">رقم KB: 4615588</span><span class="sxs-lookup"><span data-stu-id="88bbe-104">KB number: 4615588</span></span>

## <a name="symptoms"></a><span data-ttu-id="88bbe-105">العلامات</span><span class="sxs-lookup"><span data-stu-id="88bbe-105">Symptoms</span></span>

<span data-ttu-id="88bbe-106">في بعض وحدات السيناريو، قد تتلقي الرسالة التالية عند فتح الصفحة **تغطية الصنف** بعد استيراد الأصناف من خلال الكيان *تغطية الصنف V2*:</span><span class="sxs-lookup"><span data-stu-id="88bbe-106">In some scenarios, you might receive the following message when you open the **Item coverage** page after you import items through the *Item coverage V2* entity:</span></span>

> <span data-ttu-id="88bbe-107">هل تريد حفظ التغييرات قبل الإغلاق؟</span><span class="sxs-lookup"><span data-stu-id="88bbe-107">Do you want to save your changes before closing?</span></span>

<span data-ttu-id="88bbe-108">تظهر لك هذه الرسالة حتى لو لم تقم بإجراء أية تغييرات.</span><span class="sxs-lookup"><span data-stu-id="88bbe-108">You receive this message even though you haven't made any changes.</span></span>

## <a name="resolution"></a><span data-ttu-id="88bbe-109">الحل</span><span class="sxs-lookup"><span data-stu-id="88bbe-109">Resolution</span></span>

<span data-ttu-id="88bbe-110">تتضمن الصفحة **تغطية الصنف** منطق إعداد افتراضي مركب قد يؤدي إلى ظهور الرسالة بعد إجراء التغييرات المباشرة في قاعدة البيانات، مثل استيراد الكيان.</span><span class="sxs-lookup"><span data-stu-id="88bbe-110">The **Item coverage** page includes complex defaulting logic that might cause the message to be shown after direct changes have recently been made in the database, such as through entity import.</span></span> <span data-ttu-id="88bbe-111">على سبيل المثال، يتم تعيين الحقل الكيان `AREGENERALSETTINGSOVERRIDDEN` إلى *No*، لكن إنك تقوم باستيراد ملف يقدم قيم جديدة أو معدلة للحقول مثل `PRODUCTCOVERAGEGROUPID` و/أو `VENDORACCOUNTNUMBER`.</span><span class="sxs-lookup"><span data-stu-id="88bbe-111">For example, the `AREGENERALSETTINGSOVERRIDDEN` entity field is set to *No*, but you import a file that provides new or modified values for fields such as `PRODUCTCOVERAGEGROUPID` and/or `VENDORACCOUNTNUMBER`.</span></span> <span data-ttu-id="88bbe-112">في هذه الحالة، بسبب تعيين الحقل `AREGENERALSETTINGSOVERRIDDEN` إلى *لا*، يتم مسح القيم تلقائيًا من الحقول عند فتح الصفحة **تغطية الصنف** لأول مرة بعد عملية الاستيراد.</span><span class="sxs-lookup"><span data-stu-id="88bbe-112">In this case, because the `AREGENERALSETTINGSOVERRIDDEN` field is set to *No*, the values are automatically cleared from the fields when you open the **Item coverage** page for the first time after the import.</span></span> <span data-ttu-id="88bbe-113">إذا قمت بحفظ التغييرات كلما تطلب مربع الرسالة، فإنه يتم تخزينها في قاعدة البيانات.</span><span class="sxs-lookup"><span data-stu-id="88bbe-113">If you save the changes as the message box prompts, they are stored in the database.</span></span> <span data-ttu-id="88bbe-114">وإلا، ستتلقى الرسالة نفسها في المرة التالية التي تقوم فيها بفتح الصفحة.</span><span class="sxs-lookup"><span data-stu-id="88bbe-114">Otherwise, you will receive the same message the next time that you open the page.</span></span>

<span data-ttu-id="88bbe-115">لمنع هذا السلوك ولكن أيضًا لتضمين قيم للحقول مثل `PRODUCTCOVERAGEGROUPID` خلال استيراد الكيان، قم بتعيين `AREGENERALSETTINGSOVERRIDDEN` إلى *نعم* عندما تقوم بالاستيراد.</span><span class="sxs-lookup"><span data-stu-id="88bbe-115">To prevent this behavior but also include values for fields such as `PRODUCTCOVERAGEGROUPID` through entity import, set `AREGENERALSETTINGSOVERRIDDEN` to *Yes* when you import.</span></span>
