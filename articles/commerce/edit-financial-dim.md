---
title: تحرير الأبعاد المالية لمعاملات البيع بالتجزئة
description: يوضح هذا الموضوع كيفية تحرير الأبعاد المالية لمعاملات البيع بالتجزئة في Microsoft Dynamics 365 Commerce.
author: josaw1
manager: AnnBe
ms.date: 11/04/2020
ms.topic: index-page
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ed0f77f7-3609-4330-bebd-ca3134575216
ms.search.region: global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2018-11-15
ms.dyn365.ops.version: ''
ms.openlocfilehash: 5a5a82adbad16d8fea2ccf60ae0dbfbd2fd9f3c1
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 01/15/2021
ms.locfileid: "5010166"
---
# <a name="edit-financial-dimensions-for-retail-transactions"></a><span data-ttu-id="b177f-103">تحرير الأبعاد المالية لمعاملات البيع بالتجزئة</span><span class="sxs-lookup"><span data-stu-id="b177f-103">Edit financial dimensions for retail transactions</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="b177f-104">يوضح هذا الموضوع كيفية تحرير الأبعاد المالية لمعاملات البيع بالتجزئة في Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="b177f-104">This topic describes how to edit financial dimensions for retail transactions in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="edit-financial-dimensions"></a><span data-ttu-id="b177f-105">تحرير الأبعاد المالية</span><span class="sxs-lookup"><span data-stu-id="b177f-105">Edit financial dimensions</span></span>

<span data-ttu-id="b177f-106">لتحرير الأبعاد المالية لمعاملات البيع بالتجزئة في المركز الرئيسي لـ Commerce، اتبع هذه الخطوات.</span><span class="sxs-lookup"><span data-stu-id="b177f-106">To edit financial dimensions for retail transactions in Commerce headquarters, follow these steps.</span></span>

1. <span data-ttu-id="b177f-107">فتح صفحة **تكوين الأبعاد المالية لتكامل التطبيقات**.</span><span class="sxs-lookup"><span data-stu-id="b177f-107">Open the **Financial dimensions configuration for integrating applications** page.</span></span>
1. <span data-ttu-id="b177f-108">حدد **سجل تكامل الأبعاد الافتراضية** النشطة.</span><span class="sxs-lookup"><span data-stu-id="b177f-108">Select the active **Default dimensions integration** record.</span></span>
1. <span data-ttu-id="b177f-109">في علامة التبويب السريعة **الأبعاد المالية** ، تأكد من أن جميع الأبعاد التي تريد تحريرها في ورقة عمل Excel موجودة في القائمة **المحددة**.</span><span class="sxs-lookup"><span data-stu-id="b177f-109">On the **Financial dimensions** FastTab, make sure that all the dimensions that you want to edit in the Excel worksheet are present in the **Selected** list.</span></span> <span data-ttu-id="b177f-110">لمزيد من المعلومات، راجع [كيانات البيانات](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/financial/financial-dimension-configuration-integration#data-entities).</span><span class="sxs-lookup"><span data-stu-id="b177f-110">For more information, see [Data entities](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/financial/financial-dimension-configuration-integration#data-entities).</span></span>
1. <span data-ttu-id="b177f-111">قم بتنزيل ملف Excel وافتحه من صفحة **كشوف الحسابات** ، أو صفحة **معاملات البيع بالتجزئة** ، أو مربع الإطار المتجانب **إخفاقات التحقق من صحة المعاملات** في مساحة العمل **ماليات المتجر**.</span><span class="sxs-lookup"><span data-stu-id="b177f-111">Download and open the Excel file from the **Statements** page, the **Retail transactions** page, or the **Transaction validation failures** tile in the **Store financials** workspace.</span></span>
1. <span data-ttu-id="b177f-112">لتغيير البعد المالي للمعاملة، حدد **تصميم**، ثم حدد رمز القلم المجاور لصف **معاملة (قابلة للتدقيق)**.</span><span class="sxs-lookup"><span data-stu-id="b177f-112">To change the transaction financial dimension, select **Design**, and then select the pencil symbol next to the **Transaction (auditable)** row.</span></span>
1. <span data-ttu-id="b177f-113">ابحث عن الحقل **FinancialDimensionDisplayValue** وحدده، وحدد خلية في جزء الرأس بورقة عمل Excel، ثم حدد **إضافة تسمية**.</span><span class="sxs-lookup"><span data-stu-id="b177f-113">Find and select the **FinancialDimensionDisplayValue** field, select a cell in the header part of the Excel worksheet, and then select **Add label**.</span></span>
1. <span data-ttu-id="b177f-114">حدد خلية أسفل الخلية التي حددتها في الخطوة السابقة ، وحدد **إضافة قيمة**، ثم حدد **تحديث**.</span><span class="sxs-lookup"><span data-stu-id="b177f-114">Select a cell below the cell that you selected in the previous step, select **Add Value**, and then select **Refresh**.</span></span> <span data-ttu-id="b177f-115">تُضاف الأبعاد المالية إلى ورقة عمل Excel، ويمكن بعد ذلك تحريرها ونشرها.</span><span class="sxs-lookup"><span data-stu-id="b177f-115">The financial dimensions are added to the Excel worksheet, and they can then be edited and published.</span></span>
1. <span data-ttu-id="b177f-116">لتغيير الأبعاد في بنود المعاملة، حدد صف **معاملات المبيعات (قابل للتدقيق)** ، وحدد رمز القلم، ثم كرر الخطوتين 6 و7.</span><span class="sxs-lookup"><span data-stu-id="b177f-116">To change the dimensions on the transaction lines, select the **Sales transactions (auditable)** row, select the pencil symbol, and then repeat steps 6 and 7.</span></span>
1. <span data-ttu-id="b177f-117">لتغيير الأبعاد في بنود الدفع، حدد صف **معاملات الدفع (قابل للتدقيق)** ، وحدد رمز القلم، ثم كرر الخطوتين 6 و7.</span><span class="sxs-lookup"><span data-stu-id="b177f-117">To change the dimensions on the payment lines, select the **Payment transactions (auditable)** row, select the pencil symbol, and then repeat steps 6 and 7.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="b177f-118">الموارد الإضافية</span><span class="sxs-lookup"><span data-stu-id="b177f-118">Additional resources</span></span>

[<span data-ttu-id="b177f-119">تحرير وتدقيق معاملات الدفع نقدًا والاستلام فورًا وإدارة النقد</span><span class="sxs-lookup"><span data-stu-id="b177f-119">Edit and audit cash and carry and cash management transactions</span></span>](edit-cash-trans.md)

[<span data-ttu-id="b177f-120">تحرير وتدقيق الأوامر عبر الإنترنت ومعاملات أمر العميل غير المتزامنة</span><span class="sxs-lookup"><span data-stu-id="b177f-120">Edit and audit online order and asynchronous customer order transactions</span></span>](edit-order-trans.md)

[<span data-ttu-id="b177f-121">إنشاء دفتر عمل Excel لتحرير معاملات البيع بالتجزئة</span><span class="sxs-lookup"><span data-stu-id="b177f-121">Create an Excel workbook to edit retail transactions</span></span>](create-excel-edit.md)

[<span data-ttu-id="b177f-122">إضافة الحقول إلى دفتر عمل Excel لتحرير معاملات البيع بالتجزئة</span><span class="sxs-lookup"><span data-stu-id="b177f-122">Add fields to an Excel workbook to edit retail transactions</span></span>](add-fields-excel.md)
