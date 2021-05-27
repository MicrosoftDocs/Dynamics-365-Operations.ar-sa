---
title: إعداد أكواد تقرير ضريبة الخصم لنوع ضريبة TDS
description: يتم استخدام أكواد تقارير ضريبة الخصم لإنشاء كشوف نموذج 26Q ونموذج 27Q للضريبة المخصومة في المصدر (TDS). يوضح هذا الموضوع كيفية إعداد خطوات أكواد تقارير ضريبة الخصم بحيث يمكنك إعداد أكواد تقارير TDS.
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
ms.openlocfilehash: 1f9325d182f89b98e8b943ae047c55e7e1aeb02f
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 05/11/2021
ms.locfileid: "6023008"
---
# <a name="set-up-withholding-tax-reporting-codes-for-the-tds-tax-type"></a><span data-ttu-id="14591-104">إعداد أكواد تقرير ضريبة الخصم لنوع ضريبة TDS</span><span class="sxs-lookup"><span data-stu-id="14591-104">Set up withholding tax reporting codes for the TDS tax type</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="14591-105">يتم استخدام أكواد تقارير ضريبة الخصم لإنشاء كشوف نموذج 26Q ونموذج 27Q للضريبة المخصومة في المصدر (TDS).</span><span class="sxs-lookup"><span data-stu-id="14591-105">Withholding tax reporting codes are used to generate Form 26Q and Form 27Q statements for Tax Deducted at Source (TDS).</span></span> <span data-ttu-id="14591-106">يوضح هذا الموضوع كيفية إعداد خطوات أكواد تقارير ضريبة الخصم بحيث يمكنك إعداد أكواد تقارير TDS.</span><span class="sxs-lookup"><span data-stu-id="14591-106">This topic explains how to set up withholding tax reporting codes steps so that you can set up TDS reporting codes.</span></span>

1. <span data-ttu-id="14591-107">انتقل إلى **الضريبة \> الإعداد \> ضريبة الخصم \> أكواد تقرير ضريبة الخصم**.</span><span class="sxs-lookup"><span data-stu-id="14591-107">Go to **Tax \> Setup \> Withholding tax \> Withholding tax reporting codes**.</span></span>

    <span data-ttu-id="14591-108">[![صفحة أكواد تقارير ضريبة الخصم](./media/apac-ind-TDS-16.png)](./media/apac-ind-TDS-16.png)</span><span class="sxs-lookup"><span data-stu-id="14591-108">[![Withholding tax reporting codes page](./media/apac-ind-TDS-16.png)](./media/apac-ind-TDS-16.png)</span></span>

2. <span data-ttu-id="14591-109">في الحقل **نوع الضريبة**، حدد **TDS** لتحديد أكواد تقارير ضريبة الخصم لنوع الضريبة TDS.</span><span class="sxs-lookup"><span data-stu-id="14591-109">In the **Tax type** field, select **TDS** to define withholding tax reporting codes for the TDS tax type.</span></span>
3. <span data-ttu-id="14591-110">في الحقل **مكون ضريبة الخصم**، حدد مكون TDS إلى ما تقوم بتحديد كود تقارير ضريبة الخصم له.</span><span class="sxs-lookup"><span data-stu-id="14591-110">In the **Withholding tax component** field, select the TDS component to that you're defining the withholding tax reporting code for.</span></span> <span data-ttu-id="14591-111">يعرض الحقل **مجموعة مكون ضريبة الخصم** مجموعة المكون TDS التي تم تحديدها لمكون TDS الذي تقوم بتعريفه.</span><span class="sxs-lookup"><span data-stu-id="14591-111">The **Withholding tax component group** field shows the TDS component group that was defined for the TDS component that you're defining.</span></span>

    <span data-ttu-id="14591-112">يعرض الحقل **كود القسم** الموجود على علامة التبويب السريعة **عام** كود القسم الذي يتم إرفاقه بمجموعة مكون TDS.</span><span class="sxs-lookup"><span data-stu-id="14591-112">The **Section code** field on the **General** FastTab shows the section code that is attached to the TDS component group.</span></span>

4. <span data-ttu-id="14591-113">ضمن علامة التبويب السريعة **عام**، في الحقل **كود التقرير**، حدد كود تقارير TDS.</span><span class="sxs-lookup"><span data-stu-id="14591-113">On the **General** FastTab, in the **Reporting code** field, select the TDS reporting code:</span></span>

    - <span data-ttu-id="14591-114">TDS</span><span class="sxs-lookup"><span data-stu-id="14591-114">TDS</span></span>
    - <span data-ttu-id="14591-115">TCS</span><span class="sxs-lookup"><span data-stu-id="14591-115">TCS</span></span>
    - <span data-ttu-id="14591-116">رسوم إضافية</span><span class="sxs-lookup"><span data-stu-id="14591-116">Surcharge</span></span>
    - <span data-ttu-id="14591-117">PE\_Cess</span><span class="sxs-lookup"><span data-stu-id="14591-117">PE\_Cess</span></span>
    - <span data-ttu-id="14591-118">SHE\_Cess</span><span class="sxs-lookup"><span data-stu-id="14591-118">SHE\_Cess</span></span>

5. <span data-ttu-id="14591-119">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="14591-119">Close the page.</span></span>
