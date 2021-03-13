---
title: إنشاء مدفوعات ضريبة خصم
description: يعمل إجراء "مهمة مدفوعات ضريبة الخصم" على تسوية أرصدة ضريبة الخصم من الحسابات الدائنة في حسابات ضريبة الخصم وتعويضها في حساب تسوية ضريبة الخصم لفترة معينة. يسرد هذا الموضوع الخطوات الخاصة بإعداد دفع ضريبة الخصم.
author: roschlom
manager: AnnBe
ms.date: 01/12/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.custom: 15721
ms.assetid: b4b406fa-b772-44ec-8dd8-8eb818a921ef
ms.search.region: Global
ms.author: kailiang
ms.search.validFrom: 2020-01-12
ms.dyn365.ops.version: AX 10.0.16
ms.openlocfilehash: e522711340b663bd849825b3d4dd2b7e78e4737c
ms.sourcegitcommit: 630a0b3f800f36ced49b79156dd52132904fef75
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 01/25/2021
ms.locfileid: "5060697"
---
# <a name="create-a-withholding-tax-payment"></a><span data-ttu-id="5dbce-104">إنشاء مدفوعات ضريبة خصم</span><span class="sxs-lookup"><span data-stu-id="5dbce-104">Create a withholding tax payment</span></span>

<span data-ttu-id="5dbce-105">يعمل إجراء "مهمة مدفوعات ضريبة الخصم" على تسوية أرصدة ضريبة الخصم من الحسابات الدائنة في حسابات ضريبة الخصم وتعويضها في حساب تسوية ضريبة الخصم لفترة معينة.</span><span class="sxs-lookup"><span data-stu-id="5dbce-105">The Withholding tax payment job procedure settles withholding tax balances from Accounts payable on withholding tax accounts, and offsets them to the withholding tax settlement account for a given period.</span></span> <span data-ttu-id="5dbce-106">يسرد هذا الموضوع الخطوات الخاصة بإعداد دفع ضريبة الخصم.</span><span class="sxs-lookup"><span data-stu-id="5dbce-106">This topic lists the steps for setting up a withholding tax payment.</span></span>

> [!NOTE] 
> <span data-ttu-id="5dbce-107">لا يتم وضع تعويض ضريبة الخصم (من الحساب المدينة) في الاعتبار عند حساب دفع ضريبة الخصم.</span><span class="sxs-lookup"><span data-stu-id="5dbce-107">Withholding tax offset (from accounts receivable) is not taken into account when a withholding tax payment is calculated.</span></span>

1. <span data-ttu-id="5dbce-108">انتقل إلى **جزء التنقل > الوحدات النمطية > الضريبة > الإقرارات > ضريبة الخصم > دفع ضريبة الخصم**.</span><span class="sxs-lookup"><span data-stu-id="5dbce-108">Go to **Navigation pane > Modules > Tax > Declarations > Withholding tax > Withholding tax payment**.</span></span>
2. <span data-ttu-id="5dbce-109">في الحقل **فترة التسوية**، انقر فوق زر القائمة المنسدلة لفتح البحث.</span><span class="sxs-lookup"><span data-stu-id="5dbce-109">In the **Settlement period** field, click the drop-down button to open the lookup.</span></span>
3. <span data-ttu-id="5dbce-110">في القائمة، انقر فوق الارتباط في الصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="5dbce-110">In the list, click the link in the selected row.</span></span>
4. <span data-ttu-id="5dbce-111">في الحقل **من تاريخ**، أدخل تاريخًا.</span><span class="sxs-lookup"><span data-stu-id="5dbce-111">In the **From date** field, enter a date.</span></span>
5. <span data-ttu-id="5dbce-112">في حقل **‏‫تاريخ الحركة**، أدخل تاريخًا.</span><span class="sxs-lookup"><span data-stu-id="5dbce-112">In the **Transaction date** field, enter a date.</span></span>
6. <span data-ttu-id="5dbce-113">حدد **تحديث** لترحيل إيصال دفع ضريبة الخصم إلى حساب تسوية ضريبة الخصم.</span><span class="sxs-lookup"><span data-stu-id="5dbce-113">Select **Update** to post withholding tax payment voucher to the withholding tax settlement account.</span></span>
7. <span data-ttu-id="5dbce-114">انقر فوق **موافق**.</span><span class="sxs-lookup"><span data-stu-id="5dbce-114">Click **OK**.</span></span>

![المعلمات لدفع ضريبة الخصم](media/withholding-tax-payment.png)
