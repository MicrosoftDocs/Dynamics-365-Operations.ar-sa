---
title: إعداد جداول الدفع باستخدام توزيع TDS
description: يوضح هذا الموضوع كيفية إعداد جداول الدفع باستخدام توزيع الضريبة المخصومة في المصدر (TDS).
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
ms.openlocfilehash: 47551f52f35fec5ae49d696e3f4027b7d2eb2e19
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 05/11/2021
ms.locfileid: "6023006"
---
# <a name="set-up-payment-schedules-with-tds-allocation"></a><span data-ttu-id="3686e-103">إعداد جداول الدفع باستخدام توزيع TDS</span><span class="sxs-lookup"><span data-stu-id="3686e-103">Set up payment schedules with TDS allocation</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="3686e-104">يوضح هذا الموضوع كيفية إعداد جداول الدفع باستخدام توزيع الضريبة المخصومة في المصدر (TDS).</span><span class="sxs-lookup"><span data-stu-id="3686e-104">This topic explains how to set up payment schedules with Tax Deducted at Source (TDS) allocation.</span></span>

1. <span data-ttu-id="3686e-105">انتقل إلى **الحسابات المدينة \> إعداد الدفع \> جداول الدفع**.</span><span class="sxs-lookup"><span data-stu-id="3686e-105">Go to **Accounts payable \> Payment setup \> Payment schedules**.</span></span>

    <span data-ttu-id="3686e-106">[![صفحة جداول الدفع](./media/apac-ind-TDS-27.png)](./media/apac-ind-TDS-27.png)</span><span class="sxs-lookup"><span data-stu-id="3686e-106">[![Payment schedules page](./media/apac-ind-TDS-27.png)](./media/apac-ind-TDS-27.png)</span></span>

2. <span data-ttu-id="3686e-107">في جزء الإجراء، حدد **جديد** لإنشاء جدول دفع، وأدخل التفاصيل المطلوبة.</span><span class="sxs-lookup"><span data-stu-id="3686e-107">On the Action Pane, select **New** to create a payment schedule, and enter the required details.</span></span>
3. <span data-ttu-id="3686e-108">في الحقل **توزيع**، حدد الأسلوب الذي سيتم استخدامه لتوزيع الدفع لجدول الدفع:</span><span class="sxs-lookup"><span data-stu-id="3686e-108">In the **Allocation** field, select the method to use to allocate the payment for the payment schedule:</span></span>

    - <span data-ttu-id="3686e-109">الإجمالي</span><span class="sxs-lookup"><span data-stu-id="3686e-109">Total</span></span>
    - <span data-ttu-id="3686e-110">مبلغ ثابت</span><span class="sxs-lookup"><span data-stu-id="3686e-110">Fixed amount</span></span>
    - <span data-ttu-id="3686e-111">كمية ثابتة</span><span class="sxs-lookup"><span data-stu-id="3686e-111">Fixed quantity</span></span>
    - <span data-ttu-id="3686e-112">محدد</span><span class="sxs-lookup"><span data-stu-id="3686e-112">Specified</span></span>

    <span data-ttu-id="3686e-113">يعرض الحقل **توزيع ضريبة الخصم** أسلوب توزيع TDS لجدول الدفع.</span><span class="sxs-lookup"><span data-stu-id="3686e-113">The **Withholding tax allocation** field shows the TDS allocation method for the payment schedule.</span></span> <span data-ttu-id="3686e-114">إذا قمت بتحديد **الإجمالي** في الحقل **توزيع**، فإنه سيتم تعيين الحقل **توزيع ضريبة الخصم** تلقائيًا إلى **إجمالي**.</span><span class="sxs-lookup"><span data-stu-id="3686e-114">If you select **Total** in the **Allocation** field, the **Withholding tax allocation** field is automatically set to **Total**.</span></span> <span data-ttu-id="3686e-115">إذا قمت بتحديد **المبلغ الثابت** أو **الكمية الثابتة** أو **المحدد** في الحقل **توزيع**، فإنه سيتم تعيين الحقل  **توزيع ضريبة الخصم**  تلقائيًا إلى **بشكل متناسب**.</span><span class="sxs-lookup"><span data-stu-id="3686e-115">If you select **Fixed amount**, **Fixed quantity**, or **Specified** in the **Allocation** field, the **Withholding tax allocation** field is automatically set to **Proportionally**.</span></span>

    > [!NOTE]
    > <span data-ttu-id="3686e-116">في حالة تعيين الحقل **توزيع ضريبة الخصم** على **الإجمالي**، فإنه يتم حساب أقساط الدفع استنادًا إلى المبلغ الإجمالي، والذي يتضمن مبلغ TDS.</span><span class="sxs-lookup"><span data-stu-id="3686e-116">If the **Withholding tax allocation** field is set to **Total**, the payment installments are calculated based on the gross amount, which includes the TDS amount.</span></span> <span data-ttu-id="3686e-117">في حالة تعيين الحقل **توزيع ضريبة الخصم** على **بشكل متناسب**، فإنه يتم حساب أقساط الدفع استنادًا إلى صافي مبلغ الفاتورة بعد خصم مبلغ TDS.</span><span class="sxs-lookup"><span data-stu-id="3686e-117">If the **Withholding tax allocation** field is set to **Proportionally**, the payment installments are calculated based on the net invoice amount after the TDS amount is deducted.</span></span>

4. <span data-ttu-id="3686e-118">أدخل التفاصيل الأخرى المطلوبة، ثم أغلق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="3686e-118">Enter the other required details, and then close the page.</span></span>
