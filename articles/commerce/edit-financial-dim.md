---
title: تحرير الابعاد المالية لحركات البيع بالتجزئة
description: يوضح هذا الموضوع كيفية تحرير الأبعاد المالية لحركات البيع بالتجزئة في Microsoft Dynamics 365 Commerce.
author: josaw1
manager: AnnBe
ms.date: 11/04/2020
ms.topic: index-page
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Core, Operations, Retail
ms.custom: ''
ms.assetid: ed0f77f7-3609-4330-bebd-ca3134575216
ms.search.region: global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2018-11-15
ms.dyn365.ops.version: ''
ms.openlocfilehash: e26bd4eb53fa44330f15c7cda004cb3d19dfec6d
ms.sourcegitcommit: ce51ff2b6099c75dceb99de6dea9d53baf99772d
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 11/04/2020
ms.locfileid: "4458408"
---
# <a name="edit-financial-dimensions-for-retail-transactions"></a><span data-ttu-id="59465-103">تحرير الابعاد المالية لحركات البيع بالتجزئة</span><span class="sxs-lookup"><span data-stu-id="59465-103">Edit financial dimensions for retail transactions</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="59465-104">يوضح هذا الموضوع كيفية تحرير الأبعاد المالية لحركات البيع بالتجزئة في Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="59465-104">This topic describes how to edit financial dimensions for retail transactions in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="edit-financial-dimensions"></a><span data-ttu-id="59465-105">تحرير الأبعاد المالية</span><span class="sxs-lookup"><span data-stu-id="59465-105">Edit financial dimensions</span></span>

<span data-ttu-id="59465-106">لتحرير الأبعاد المالية لمعاملات البيع بالتجزئة في المركز الرئيسي لـ Commerce، اتبع هذه الخطوات.</span><span class="sxs-lookup"><span data-stu-id="59465-106">To edit financial dimensions for retail transactions in Commerce headquarters, follow these steps.</span></span>

1. <span data-ttu-id="59465-107">فتح صفحة **تكوين الأبعاد المالية لتكامل التطبيقات**.</span><span class="sxs-lookup"><span data-stu-id="59465-107">Open the **Financial dimensions configuration for integrating applications** page.</span></span>
1. <span data-ttu-id="59465-108">حدد **سجل تكامل الابعاد الافتراضية** النشطة.</span><span class="sxs-lookup"><span data-stu-id="59465-108">Select the active **Default dimensions integration** record.</span></span>
1. <span data-ttu-id="59465-109">في علامة التبويب السريعة **الأبعاد المالية** ، تأكد من أن جميع الأبعاد التي تريد تحريرها في ورقة عمل Excel موجودة في القائمة **المحددة**.</span><span class="sxs-lookup"><span data-stu-id="59465-109">On the **Financial dimensions** FastTab, make sure that all the dimensions that you want to edit in the Excel worksheet are present in the **Selected** list.</span></span> <span data-ttu-id="59465-110">لمزيد من المعلومات، راجع [كيانات البيانات](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/financial/financial-dimension-configuration-integration#data-entities).</span><span class="sxs-lookup"><span data-stu-id="59465-110">For more information, see [Data entities](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/financial/financial-dimension-configuration-integration#data-entities).</span></span>
1. <span data-ttu-id="59465-111">قم بتنزيل ملف Excel وافتحه من صفحة **كشوف الحسابات** ، أو صفحة **حركات البيع بالتجزئة** ، أو مربع الإطار المتجانب **إخفاقات التحقق من صحة الحركات** في مساحة العمل **ماليات المتجر**.</span><span class="sxs-lookup"><span data-stu-id="59465-111">Download and open the Excel file from the **Statements** page, the **Retail transactions** page, or the **Transaction validation failures** tile in the **Store financials** workspace.</span></span>
1. <span data-ttu-id="59465-112">لتغيير البعد المالي للحركة، حدد **تصميم**، ثم حدد رمز القلم المجاور لصف **حركة (قابلة للتدقيق)**.</span><span class="sxs-lookup"><span data-stu-id="59465-112">To change the transaction financial dimension, select **Design**, and then select the pencil symbol next to the **Transaction (auditable)** row.</span></span>
1. <span data-ttu-id="59465-113">ابحث عن الحقل **FinancialDimensionDisplayValue** وحدده، وحدد خلية في جزء الرأس بورقة عمل Excel، ثم حدد **إضافة تسمية**.</span><span class="sxs-lookup"><span data-stu-id="59465-113">Find and select the **FinancialDimensionDisplayValue** field, select a cell in the header part of the Excel worksheet, and then select **Add label**.</span></span>
1. <span data-ttu-id="59465-114">حدد خلية أسفل الخلية التي حددتها في الخطوة السابقة ، وحدد **إضافة قيمة**، ثم حدد **تحديث**.</span><span class="sxs-lookup"><span data-stu-id="59465-114">Select a cell below the cell that you selected in the previous step, select **Add Value**, and then select **Refresh**.</span></span> <span data-ttu-id="59465-115">تُضاف الأبعاد المالية إلى ورقة عمل Excel، ويمكن بعد ذلك تحريرها ونشرها.</span><span class="sxs-lookup"><span data-stu-id="59465-115">The financial dimensions are added to the Excel worksheet, and they can then be edited and published.</span></span>
1. <span data-ttu-id="59465-116">لتغيير الابعاد في بنود الحركة، حدد صف **حركات المبيعات (قابل للتدقيق)** ، وحدد رمز القلم، ثم كرر الخطوتين 6 و7.</span><span class="sxs-lookup"><span data-stu-id="59465-116">To change the dimensions on the transaction lines, select the **Sales transactions (auditable)** row, select the pencil symbol, and then repeat steps 6 and 7.</span></span>
1. <span data-ttu-id="59465-117">لتغيير الابعاد في بنود الدفع، حدد صف **حركات الدفع (قابل للتدقيق)** ، وحدد رمز القلم، ثم كرر الخطوتين 6 و7.</span><span class="sxs-lookup"><span data-stu-id="59465-117">To change the dimensions on the payment lines, select the **Payment transactions (auditable)** row, select the pencil symbol, and then repeat steps 6 and 7.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="59465-118">الموارد الإضافية</span><span class="sxs-lookup"><span data-stu-id="59465-118">Additional resources</span></span>

[<span data-ttu-id="59465-119">تحرير وتدقيق حركات الدفع نقدًا والاستلام فورًا وإدارة النقد</span><span class="sxs-lookup"><span data-stu-id="59465-119">Edit and audit cash and carry and cash management transactions</span></span>](edit-cash-trans.md)

[<span data-ttu-id="59465-120">تحرير وتدقيق الأوامر عبر الإنترنت وحركات أمر العميل غير المتزامنة</span><span class="sxs-lookup"><span data-stu-id="59465-120">Edit and audit online order and asynchronous customer order transactions</span></span>](edit-order-trans.md)

[<span data-ttu-id="59465-121">إنشاء مصنف Excel لتحرير حركات البيع بالتجزئة</span><span class="sxs-lookup"><span data-stu-id="59465-121">Create an Excel workbook to edit retail transactions</span></span>](create-excel-edit.md)

[<span data-ttu-id="59465-122">إضافة الحقول إلى مصنف Excel لتحرير حركات البيع بالتجزئة</span><span class="sxs-lookup"><span data-stu-id="59465-122">Add fields to an Excel workbook to edit retail transactions</span></span>](add-fields-excel.md)
