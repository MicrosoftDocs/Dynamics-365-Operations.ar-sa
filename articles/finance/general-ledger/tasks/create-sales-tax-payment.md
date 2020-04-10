---
title: إنشاء دفع ضريبة مبيعات
description: تعمل وظيفة "تسوية ضريبة المبيعات وترحيلها‬" على تسوية أرصدة ضريبة المبيعات على حسابات ضريبة المبيعات وتعويضها في حساب تسوية ضريبة المبيعات لفترة معينة.
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
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: vstehman
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 99059a8e5d6f4bf125266ad2a98cb73751529e6b
ms.sourcegitcommit: 57e1dafa186fec77ddd8ba9425d238e36e0f0998
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 03/18/2020
ms.locfileid: "3139911"
---
# <a name="create-a-sales-tax-payment"></a><span data-ttu-id="6017b-103">إنشاء دفع ضريبة مبيعات</span><span class="sxs-lookup"><span data-stu-id="6017b-103">Create a sales tax payment</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="6017b-104">تعمل وظيفة "تسوية ضريبة المبيعات وترحيلها‬" على تسوية أرصدة ضريبة المبيعات على حسابات ضريبة المبيعات وتعويضها في حساب تسوية ضريبة المبيعات لفترة معينة.</span><span class="sxs-lookup"><span data-stu-id="6017b-104">The settle and post sales tax job settles sales tax balances on the sales tax accounts and offsets them to the sales tax settlement account for a given period.</span></span>

1. <span data-ttu-id="6017b-105">انتقل إلى الضريبة > إقرارات > ضريبة المبيعات > تسوية ضريبة المبيعات وترحيلها‬‬.</span><span class="sxs-lookup"><span data-stu-id="6017b-105">Go to Tax > Declarations > Sales tax > Settle and post sales tax.</span></span>
2. <span data-ttu-id="6017b-106">في الحقل "فترة التسوية"، انقر فوق زر القائمة المنسدلة لفتح البحث.</span><span class="sxs-lookup"><span data-stu-id="6017b-106">In the Settlement period field, click the drop-down button to open the lookup.</span></span>
3. <span data-ttu-id="6017b-107">في القائمة، انقر فوق الارتباط في الصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="6017b-107">In the list, click the link in the selected row.</span></span>
4. <span data-ttu-id="6017b-108">في الحقل "من تاريخ"، أدخل تاريخًا.</span><span class="sxs-lookup"><span data-stu-id="6017b-108">In the From date field, enter a date.</span></span>
    * <span data-ttu-id="6017b-109">إذا لم يكن الخيار "تضمين التصحيحات‬" محددًا على صفحة محددات دفتر الأستاذ العام، فيمكن معالجة التسوية لإصدارات المختلفة.</span><span class="sxs-lookup"><span data-stu-id="6017b-109">If the Include corrections option is not selected on the General ledger parameters page, the settlement can be processed for different versions.</span></span> <span data-ttu-id="6017b-110">الإصدار الأصلي هو التسوية الأولى لفترة زمنية ولا يمكن معالجته إلا مرة واحدة لفترة زمنية.</span><span class="sxs-lookup"><span data-stu-id="6017b-110">Original is the first settlement for a period interval and can only processed once for a period interval.</span></span> <span data-ttu-id="6017b-111">ستقوم أحدث التصحيحات بتسوية حركات ضريبة المبيعات التي تم ترحيلها بعد إنشاء الإصدار الأصلي.</span><span class="sxs-lookup"><span data-stu-id="6017b-111">Latest corrections will settle sales tax transactions which have been posted after the original version has been created.</span></span>   
5. <span data-ttu-id="6017b-112">في حقل "‏‫تاريخ الحركة"، أدخل تاريخًا.</span><span class="sxs-lookup"><span data-stu-id="6017b-112">In the Transaction date field, enter a date.</span></span>
6. <span data-ttu-id="6017b-113">انقر فوق "موافق".</span><span class="sxs-lookup"><span data-stu-id="6017b-113">Click OK.</span></span>

