---
title: لا تتم مراعاة إعدادات قاعدة التفريغ في بنود قائمة مكونات الصنف (BOM)‬
description: لا تتم مراعاة إعدادات قاعدة التفريغ في بنود قائمة مكونات الصنف (BOM)‬.
author: johanhoffmann
ms.date: 4/11/2021
ms.topic: troubleshooting
ms.search.form: PurchTable,ProdParameters
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2021-04-11
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: 84a84728016119a2a02f59f6903171afbceb48e7
ms.sourcegitcommit: c011a2ef66b38e71ddaf003f7d243677bb2707c5
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 05/12/2021
ms.locfileid: "6026237"
---
# <a name="flushing-principle-settings-on-bom-lines-arent-respected"></a><span data-ttu-id="a69b1-103">لا تتم مراعاة إعدادات قاعدة التفريغ في بنود قائمة مكونات الصنف (BOM)‬</span><span class="sxs-lookup"><span data-stu-id="a69b1-103">Flushing principle settings on BOM lines aren't respected</span></span>

<span data-ttu-id="a69b1-104">رقم KB: 4612725</span><span class="sxs-lookup"><span data-stu-id="a69b1-104">KB number: 4612725</span></span>

## <a name="symptoms"></a><span data-ttu-id="a69b1-105">العلامات</span><span class="sxs-lookup"><span data-stu-id="a69b1-105">Symptoms</span></span>

<span data-ttu-id="a69b1-106">تحدث هذه المشكلة عند تعيين الحقل **استهلاك قائمة مكونات الصنف تلقائيًا** على علامة التبويب **التحديث التلقائي** في الصفحة **معلمات التحكم في الإنتاج** إلى *قاعدة التفريغ*.</span><span class="sxs-lookup"><span data-stu-id="a69b1-106">This issue occurs when the **Automatic BOM consumption** field on the **Automatic update** tab of the **Production control parameters** page is set to *Flushing principle*.</span></span> <span data-ttu-id="a69b1-107">يشير هذا الإعداد إلى أنه يجب استهلاك كافة بنود قائمة مكونات الصنف (BOM) تلقائيًا عند استلام أمر شراء.</span><span class="sxs-lookup"><span data-stu-id="a69b1-107">This setting indicates that all bill of materials (BOM) lines should automatically be consumed when a purchase order is received.</span></span> <span data-ttu-id="a69b1-108">إذا تم تعيين الحقل **قاعدة التفريغ‬** في بنود قائمة مكونات الصنف (BOM)‬ بشكل واضح إلى *يدوي* ، فقد تتوقع عدم استهلاك بنود قائمة مكونات الصنف (BOM)‬ تلقائيًا.</span><span class="sxs-lookup"><span data-stu-id="a69b1-108">If the **Flushing principle** field on BOM lines is explicitly set to *Manual*, you might expect that the BOM lines won't automatically be consumed.</span></span> <span data-ttu-id="a69b1-109">ومع ذلك، عند حدوث هذه المشكلة، يتم استهلاك بنود قائمة مكونات الصنف (BOM)‬ حيث يتم تعيين الحقل **قاعدة التفريغ** على *يدوي* على أية حال.</span><span class="sxs-lookup"><span data-stu-id="a69b1-109">However, when this issue occurs, BOM lines where the **Flushing principle** field is set to *Manual* are automatically consumed anyway.</span></span>

## <a name="resolution"></a><span data-ttu-id="a69b1-110">الدقة</span><span class="sxs-lookup"><span data-stu-id="a69b1-110">Resolution</span></span>

<span data-ttu-id="a69b1-111">في حالة مواجهة هذه المشكلة، قد يتم إعداد معلمات التحكم في الإنتاج لتجاوز الإعداد **قاعدة التفريغ** في بنود قائمة مكونات الصنف.</span><span class="sxs-lookup"><span data-stu-id="a69b1-111">If you're experiencing this issue, your production control parameters might be set up to override the **Flushing principle** setting on BOM lines.</span></span> <span data-ttu-id="a69b1-112">في الصفحة **معلمات التحكم في الإنتاج**، من علامة التبويب **التحديث التلقائي**، تحقق من قيمة الحقل **‏‫استهلاك قائمة مكونات الصنف التلقائي‬**.</span><span class="sxs-lookup"><span data-stu-id="a69b1-112">On the **Production control parameters** page, on the **Automatic update** tab, check the value of the **Automatic BOM consumption** field.</span></span> <span data-ttu-id="a69b1-113">وإذا تم تعيينها على *دائمًا*، سيقوم النظام بتجاهل الإعداد **قاعدة التفريغ** في كافة ‏‫بنود قائمة مكونات الصنف وسيتم تفريغ البنود دائمًا.</span><span class="sxs-lookup"><span data-stu-id="a69b1-113">If it's set to *Always*, the system will disregard the **Flushing principle** setting on all BOM lines and will always flush the lines.</span></span> <span data-ttu-id="a69b1-114">لكي يقوم النظام بمراعاة الإعداد **قاعدة التفريغ** في ‏‫بنود قائمة مكونات الصنف، قم بتغيير قيمة الحقل **‏‫استهلاك قائمة مكونات الصنف التلقائي** إلى *قاعدة التفريغ*.</span><span class="sxs-lookup"><span data-stu-id="a69b1-114">To make the system respect the **Flushing principle** setting on BOM lines, change the value of the **Automatic BOM consumption** field to *Flushing principle*.</span></span>
