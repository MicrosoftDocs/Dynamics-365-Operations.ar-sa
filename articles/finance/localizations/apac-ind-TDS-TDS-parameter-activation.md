---
title: إعداد معلمات TDS
description: يشرح هذا الموضوع كيفية تعيين المعلمات لتنشيط وظيفة الضريبة المخصومة في المصدر (TDS) في حركات محددة. هذه الخطوة ضرورية لاستخدام ميزة الضريبة المخصومة في المصدر TDS.
author: kailiang
ms.date: 02/12/2021
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
ms.search.validFrom: 2021-02-12
ms.dyn365.ops.version: AX 10.0.17
ms.openlocfilehash: dda276b7d634317aae26728f7d9f51af9ccfb896
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 05/11/2021
ms.locfileid: "6022996"
---
# <a name="set-the-tds-parameters"></a><span data-ttu-id="532e5-104">إعداد معلمات TDS</span><span class="sxs-lookup"><span data-stu-id="532e5-104">Set the TDS parameters</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="532e5-105">يشرح هذا الموضوع كيفية تعيين المعلمات لتنشيط وظيفة الضريبة المخصومة في المصدر (TDS) في حركات محددة.</span><span class="sxs-lookup"><span data-stu-id="532e5-105">This topic explains how to set parameters to activate Tax Deducted at Source (TDS) functionality in specified transactions.</span></span> <span data-ttu-id="532e5-106">هذه الخطوة ضرورية لاستخدام ميزة الضريبة المخصومة في المصدر TDS.</span><span class="sxs-lookup"><span data-stu-id="532e5-106">This is a necessary step to use the Tax Deducted at Source TDS feature.</span></span>

1. <span data-ttu-id="532e5-107">انتقل إلى **دفتر الأستاذ العام \> إعداد دفتر الأستاذ‬ \> معلمات دفتر الأستاذ العام**.</span><span class="sxs-lookup"><span data-stu-id="532e5-107">Go to **General ledger \> Ledger setup \> General ledger parameters**.</span></span>
2. <span data-ttu-id="532e5-108">في علامة التبويب **الضرائب المباشرة**، في القسم **الضريبة المخصومة في المصدر**، قم بتعيين الخيار **تنشيط TDS** إلى **نعم** لتنشيط وظيفة TDS، والصفحات والحقول التي يتم استخدامها له.</span><span class="sxs-lookup"><span data-stu-id="532e5-108">On the **Direct taxes** tab, in the **Tax Deducted at Source** section, set the **Activate TDS** option to **Yes** to activate the TDS functionality, and the pages and fields that are used for it.</span></span>
3. <span data-ttu-id="532e5-109">قم بتعيين الخيار **الفاتورة** على **نعم** لتنشيط الحقول المستخدمة في حساب وخصم TDS على مستوى الفاتورة.</span><span class="sxs-lookup"><span data-stu-id="532e5-109">Set the **Invoice** option to **Yes** to activate the fields that are used to calculate and deduct TDS at the invoice level.</span></span>
4. <span data-ttu-id="532e5-110">قم بتعيين الخيار **المدفوعات** على **نعم** لتنشيط الحقول المستخدمة في حساب وخصم TDS على مستوى المدفوعات.</span><span class="sxs-lookup"><span data-stu-id="532e5-110">Set the **Payment** option to **Yes** to activate the fields that are used to calculate and deduct TDS at the payment level.</span></span>

    <span data-ttu-id="532e5-111">[![علامة التبويب الضرائب المباشرة](./media/apac-ind-TDS-1.png)](./media/apac-ind-TDS-1.png)</span><span class="sxs-lookup"><span data-stu-id="532e5-111">[![Direct taxes tab](./media/apac-ind-TDS-1.png)](./media/apac-ind-TDS-1.png)</span></span>

5. <span data-ttu-id="532e5-112">من علامة التبويب **التسلسلات الرقمية**، ابحث عن الصف الذي يتم تعيين الحقل **المرجع** فيه إلى **دفع ضريبة الخصم**.</span><span class="sxs-lookup"><span data-stu-id="532e5-112">On the **Number sequences** tab, find the row where the **Reference** field is set to **Withholding tax payment**.</span></span> <span data-ttu-id="532e5-113">ثم في الحقل **كود التسلسل الرقمي**، كود التسلسل الرقمي.</span><span class="sxs-lookup"><span data-stu-id="532e5-113">In the **Number sequence code** field for the row, select the number sequence code.</span></span> <span data-ttu-id="532e5-114">يتم استخدام كود التسلسل الرقمي لإنشاء أرقام إيصالات لعملية تسوية TDS الدورية.</span><span class="sxs-lookup"><span data-stu-id="532e5-114">The number sequence code is used to generate voucher numbers for the periodic TDS settlement process.</span></span>

    > [!NOTE]
    > <span data-ttu-id="532e5-115">لتشغيل عملية تسوية TDS الدورية، انتقل إلى **الضريبة \> الإقرارات \> ضريبة الخصم \> دفع ضريبة الخصم**.</span><span class="sxs-lookup"><span data-stu-id="532e5-115">To run the periodic TDS settlement process, go to **Tax \> Declarations \> Withholding tax \> Withholding tax payment**.</span></span>

    <span data-ttu-id="532e5-116">[![علامة التبويب التسلسلات الرقمية](./media/apac-ind-TDS-2.png)](./media/apac-ind-TDS-2.png)</span><span class="sxs-lookup"><span data-stu-id="532e5-116">[![Number sequences tab](./media/apac-ind-TDS-2.png)](./media/apac-ind-TDS-2.png)</span></span>

6. <span data-ttu-id="532e5-117">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="532e5-117">Close the page.</span></span>
