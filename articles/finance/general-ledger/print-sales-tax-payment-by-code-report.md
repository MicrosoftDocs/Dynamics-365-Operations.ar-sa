---
title: طباعة تقرير دفع ضريبة المبيعات حسب الكود‬‏‫
description: يوفر هذا الموضوع معلومات حول الإعدادات والإجراءات المطلوبة لطباعة تقرير دفع ضريبة المبيعات حسب الكود‬‏‫ بعملة الكود الضريبي أو كود المحاسبة.
author: anasyash
ms.date: 05/27/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: anasyash
ms.search.validFrom: 2020-04-08
ms.dyn365.ops.version: 10.0.11
ms.openlocfilehash: eb3ee4a12d2d29c2769f1ae22e11dc05608b47c1
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 04/01/2021
ms.locfileid: "5815442"
---
# <a name="print-the-sales-tax-payment-by-code-report"></a><span data-ttu-id="44ccb-103">طباعة تقرير دفع ضريبة المبيعات حسب الكود‬‏‫</span><span class="sxs-lookup"><span data-stu-id="44ccb-103">Print the Sales tax payment by code report</span></span> 

[!include [banner](../includes/banner.md)]

<span data-ttu-id="44ccb-104">لطباعة تقرير **دفع ضريبة المبيعات حسب الكود**، انتقل إلى **الضريبة** \> **الاستعلامات والتقارير** \> **تقارير ضرائب المبيعات** \> **دفع ضريبة المبيعات حسب الكود**.</span><span class="sxs-lookup"><span data-stu-id="44ccb-104">To print the **Sales tax payment by code** report, go to **Tax** \> **Inquiries and reports** \> **Sales tax reports** \> **Sales tax payment by code**.</span></span> <span data-ttu-id="44ccb-105">بشكل افتراضي، يتم إنشاء مبالغ التقرير بعملة المحاسبة للكيان القانوني لكافة أكواد التقارير التي يتم إعدادها في صفحة **أكواد تقارير ضريبة المبيعات**.</span><span class="sxs-lookup"><span data-stu-id="44ccb-105">By default, report amounts are generated in the accounting currency of the legal entity for all reporting codes that are set up on the **Sales tax reporting codes** page.</span></span>

<span data-ttu-id="44ccb-106">يمكنك أيضًا إنشاء هذا التقرير بحيث يعرض مبالغ دفع ضريبة المبيعات بعملات أكواد ضريبة المبيعات لجميع أكوار التقارير المعينة إلى أكواد ضريبة المبيعات على صفحة **أكواد ضريبة المبيعات**.</span><span class="sxs-lookup"><span data-stu-id="44ccb-106">You can also generate this report so that it shows the sales tax payment amounts in the currencies of sales tax codes for all reporting codes that are assigned to sales tax codes on the **Sales tax codes** page.</span></span>

## <a name="turn-on-the-feature"></a><span data-ttu-id="44ccb-107">تشغيل الميزة</span><span class="sxs-lookup"><span data-stu-id="44ccb-107">Turn on the feature</span></span>

<span data-ttu-id="44ccb-108">في مساحة عمل **إدارة الميزات**، قم بتشغيل الميزة التالية: **إنشاء تقرير دفع ضريبة المبيعات حسب الكود بعملة كود ضريبة المبيعات**.</span><span class="sxs-lookup"><span data-stu-id="44ccb-108">In the **Feature management** workspace, turn on the following feature: **Generate the Sales tax payment by code report in the sales tax code currency**.</span></span>

## <a name="run-the-report"></a><span data-ttu-id="44ccb-109">تشغيل التقرير</span><span class="sxs-lookup"><span data-stu-id="44ccb-109">Run the report</span></span>

1. <span data-ttu-id="44ccb-110">انتقل إلى **الضريبة** \> **الاستعلامات والتقارير‬** \> **تقارير ضريبة المبيعات** \> **دفع ضريبة المبيعات حسب الكود**.</span><span class="sxs-lookup"><span data-stu-id="44ccb-110">Go to **Tax** \> **Inquiries and reports** \> **Sales tax reports** \> **Sales tax payment by code**.</span></span>
2. <span data-ttu-id="44ccb-111">في حقل **عملة التقرير**، حدد إحدى القيم التالية:</span><span class="sxs-lookup"><span data-stu-id="44ccb-111">In the **Report currency** field, select one of the following values:</span></span>

    - <span data-ttu-id="44ccb-112">**عملة المحاسبة** – طباعه مبالغ التقرير بعملة المحاسبة.</span><span class="sxs-lookup"><span data-stu-id="44ccb-112">**Accounting currency** – Print the report amounts in the accounting currency.</span></span>
    - <span data-ttu-id="44ccb-113">**عملة كود ضريبة المبيعات** – طباعه مبالغ التقرير بعملات أكواد ضريبة المبيعات.</span><span class="sxs-lookup"><span data-stu-id="44ccb-113">**Sales tax code currency** – Print the report amounts in the currencies of sales tax codes.</span></span>

    ![مربع الحوار "دفع ضريبة المبيعات حسب الكود"](media/Sales-tax-payment-by-code.png)

<span data-ttu-id="44ccb-115">يبين الرسم التوضيحي التالي مثالاً للتقرير الذي يجري إنشاؤه.</span><span class="sxs-lookup"><span data-stu-id="44ccb-115">The following illustration shows an example of the report that is generated.</span></span> <span data-ttu-id="44ccb-116">يبين التقرير أن كود التقرير **101** يتضمن العملة **يورو** إذا تم تعيين الحقل **عملية ضريبة المبيعات** إلى **يورو‏‎** لكود ضريبة المبيعات الذي تم تعيين كود التقارير له.</span><span class="sxs-lookup"><span data-stu-id="44ccb-116">The report shows that reporting code **101** has the **EUR** currency if the **Sales tax currency** field is set to **EUR** for the sales tax code that the reporting code is assigned to.</span></span>

![مثال لتقرير دفع ضريبة المبيعات حسب الكود](media/Sales-tax-payment-by-code-2.png)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]