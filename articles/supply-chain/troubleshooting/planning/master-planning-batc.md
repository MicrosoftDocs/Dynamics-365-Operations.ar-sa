---
title: لا يمكنك تصفية أصناف التخطيط الرئيسي حسب قيم مجموعة التغطية المرتبطة بها
description: لا يمكنك تصفية أصناف التخطيط الرئيسي حسب قيم مجموعة التغطية المرتبطة بها.
author: ChristianRytt
ms.date: 4/11/2021
ms.topic: troubleshooting
ms.search.form: ReqTransPo
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: ilebedev
ms.search.validFrom: 2021-04-11
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: fa0b614b6710c65811add8725a0e255ce2c34b88
ms.sourcegitcommit: 3c15a26e9708adc9a75082dc551f0a3a0a7d89f4
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 05/17/2021
ms.locfileid: "6049451"
---
# <a name="you-cant-filter-master-planning-items-by-their-related-coverage-group-values"></a><span data-ttu-id="ed742-103">لا يمكنك تصفية أصناف التخطيط الرئيسي حسب قيم مجموعة التغطية المرتبطة بها</span><span class="sxs-lookup"><span data-stu-id="ed742-103">You can't filter master planning items by their related coverage group values</span></span>

<span data-ttu-id="ed742-104">رقم KB: 4612572</span><span class="sxs-lookup"><span data-stu-id="ed742-104">KB number: 4612572</span></span>

## <a name="symptoms"></a><span data-ttu-id="ed742-105">العلامات</span><span class="sxs-lookup"><span data-stu-id="ed742-105">Symptoms</span></span>

<span data-ttu-id="ed742-106">إنك ترغب في تصفية الأصناف التي سيتم تضمينها في وظيفة دُفعة التخطيط الرئيسي، وذلك استنادًا إلى قيم السجلات المرتبطة من جدول تغطية الصنف.</span><span class="sxs-lookup"><span data-stu-id="ed742-106">You want to filter the items that will be included in a master planning batch job, based on the values of related records from the item coverage table.</span></span> <span data-ttu-id="ed742-107">(على سبيل المثال، إذا كنت تريد تصفية الأصناف حسب **المورد** و/أو قيمة **مجموعة التغطية**).</span><span class="sxs-lookup"><span data-stu-id="ed742-107">(For example, you want to filter items by their **Vendor** and/or **Coverage group** value).</span></span> <span data-ttu-id="ed742-108">يتيح لك إعداد التصفية لوظيفة الدُفعة إنشاء صلة من جدول **الأصناف** إلى الجدول **تغطية الصنف**، ثم تحديد قيم الحقول من جدول تغطية الصنف في الاستعلام الخاص بك.</span><span class="sxs-lookup"><span data-stu-id="ed742-108">The filter setup for the batch job lets you create a join from the **Items** table to the **Item coverage** table, and then specify field values from the item coverage table in your query.</span></span> <span data-ttu-id="ed742-109">ومع ذلك، بعد إكمال هذا الإعداد، لا يزال النظام يقوم بإنشاء أوامر مخططة لتغطية الصنف بالكامل، وليس فقط للأصناف التي تطابق قيم الحقول المحددة من جدول تغطية الصنف.</span><span class="sxs-lookup"><span data-stu-id="ed742-109">However, after you complete this setup, the system still creates planned orders for the whole item coverage, not just for the items that match the specified field values from the item coverage table.</span></span>

## <a name="resolution"></a><span data-ttu-id="ed742-110">الحل</span><span class="sxs-lookup"><span data-stu-id="ed742-110">Resolution</span></span>

<span data-ttu-id="ed742-111">يمكن لعامل تصفية وظيفة الدُفعة إجراء التصفية على الأصناف فقط.</span><span class="sxs-lookup"><span data-stu-id="ed742-111">The batch job filter can filter only on items.</span></span> <span data-ttu-id="ed742-112">على الرغم من أنه يمكنك إضافة صلة إلى جدول **تغطية الصنف**، فإن إعدادات عامل التصفية التي تقوم بإجرائها على هذا الجدول لن تؤثر على مخرجات الاستعلام.</span><span class="sxs-lookup"><span data-stu-id="ed742-112">Although you can add a join to the **Item coverage** table, filter settings that you make against that table won't affect the query output.</span></span> <span data-ttu-id="ed742-113">في وقت التشغيل، يقوم النظام بتشغيل التخطيط لكافة مجموعات التغطية وكافة التباينات التي تشتمل عليها الأصناف التي تمت تصفيتها.</span><span class="sxs-lookup"><span data-stu-id="ed742-113">At runtime, the system runs planning for all the coverage groups and all the variations that the filtered items have.</span></span> <span data-ttu-id="ed742-114">وبعد أن يتم بالفعل تضمين أحد الأصناف في التشغيل، لن تؤثر أية مجموعات تغطية مضمنة في عامل تصفية الصنف على مخرجات التخطيط.</span><span class="sxs-lookup"><span data-stu-id="ed742-114">After an item is already included in the run, any coverage groups that are included in the item filter a won't affect the planning output.</span></span>
