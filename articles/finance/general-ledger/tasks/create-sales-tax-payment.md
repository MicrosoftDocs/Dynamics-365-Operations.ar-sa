---
title: إنشاء دفع ضريبة مبيعات
description: يعمل إجراء "تسوية ضريبة المبيعات وترحيلها‬" على تسوية أرصدة ضريبة المبيعات على حسابات ضريبة المبيعات وتعويضها في حساب تسوية ضريبة المبيعات لفترة معينة.
author: twheeloc
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: Dialog
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: roschlom
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: f9523ef75953bdca36f509f596c51c08b12b3fdb
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 02/15/2021
ms.locfileid: "5254453"
---
# <a name="create-a-sales-tax-payment"></a><span data-ttu-id="ffd51-103">إنشاء دفع ضريبة مبيعات</span><span class="sxs-lookup"><span data-stu-id="ffd51-103">Create a sales tax payment</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="ffd51-104">يعمل إجراء "تسوية ضريبة المبيعات وترحيلها‬" على تسوية أرصدة ضريبة المبيعات على حسابات ضريبة المبيعات، وتعويضها في حساب تسوية ضريبة المبيعات لفترة معينة.</span><span class="sxs-lookup"><span data-stu-id="ffd51-104">The settle and post sales tax job procedure settles sales tax balances on the sales tax accounts, and offsets them to the sales tax settlement account for a given period.</span></span>

1. <span data-ttu-id="ffd51-105">انتقل إلى **الضريبة > إقرارات > ضريبة المبيعات > تسوية ضريبة المبيعات وترحيلها**.</span><span class="sxs-lookup"><span data-stu-id="ffd51-105">Go to **Tax > Declarations > Sales tax > Settle and post sales tax**.</span></span>
2. <span data-ttu-id="ffd51-106">في الحقل **فترة التسوية**، انقر فوق زر القائمة المنسدلة لفتح البحث.</span><span class="sxs-lookup"><span data-stu-id="ffd51-106">In the **Settlement period** field, click the drop-down button to open the lookup.</span></span>
3. <span data-ttu-id="ffd51-107">في القائمة، انقر فوق الارتباط في الصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="ffd51-107">In the list, click the link in the selected row.</span></span>
4. <span data-ttu-id="ffd51-108">في الحقل **من تاريخ**، أدخل تاريخًا.</span><span class="sxs-lookup"><span data-stu-id="ffd51-108">In the **From date** field, enter a date.</span></span>
    * <span data-ttu-id="ffd51-109">إذا لم تقم بتحديد الخيار **تضمين التصحيحات** على الصفحة **معلمات دفتر الأستاذ العام**، فيمكن معالجة التسوية لإصدارات المختلفة.</span><span class="sxs-lookup"><span data-stu-id="ffd51-109">If you don't select the **Include corrections** option on the **General ledger parameters** page, the settlement can be processed for different versions.</span></span> <span data-ttu-id="ffd51-110">الإصدار الأصلي هو التسوية الأولى لفترة زمنية ولا يمكن معالجته إلا مرة واحدة لفترة زمنية.</span><span class="sxs-lookup"><span data-stu-id="ffd51-110">Original is the first settlement for a period interval and can be processed only once for a period interval.</span></span> <span data-ttu-id="ffd51-111">ستقوم أحدث التصحيحات بتسوية حركات ضريبة المبيعات التي تم ترحيلها بعد إنشاء الإصدار الأصلي.</span><span class="sxs-lookup"><span data-stu-id="ffd51-111">The latest corrections will settle sales tax transactions which have been posted after the original version has been created.</span></span>   
5. <span data-ttu-id="ffd51-112">في حقل **‏‫تاريخ الحركة**، أدخل تاريخًا.</span><span class="sxs-lookup"><span data-stu-id="ffd51-112">In the **Transaction date** field, enter a date.</span></span>
6. <span data-ttu-id="ffd51-113">انقر فوق **موافق**.</span><span class="sxs-lookup"><span data-stu-id="ffd51-113">Click **OK**.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]