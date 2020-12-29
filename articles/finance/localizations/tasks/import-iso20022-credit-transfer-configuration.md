---
title: استيراد تكوين تحويل الائتمان ISO20022
description: يوضح هذا الإجراء كيفية استيراد تكوين التقارير الإلكترونية لمدفوعات المورّد.‬
author: mrolecki
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ERWorkspace, ERVendorPart, ERSolutionRepositoryTable, ERSolutionImport
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mrolecki
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 01f44c49b6623cbcc2f08cfd6e4978c9a1676b83
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 10/13/2020
ms.locfileid: "4439993"
---
# <a name="import-iso20022-credit-transfer-configuration"></a><span data-ttu-id="42cb4-103">استيراد تكوين تحويل الائتمان ISO20022</span><span class="sxs-lookup"><span data-stu-id="42cb4-103">Import ISO20022 credit transfer configuration</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="42cb4-104">يوضح هذا الإجراء كيفية استيراد تكوين التقارير الإلكترونية لمدفوعات المورّد.‬</span><span class="sxs-lookup"><span data-stu-id="42cb4-104">This procedure shows how to import a vendor payment electronic reporting configuration.</span></span> <span data-ttu-id="42cb4-105">يتم استخدام تنسيق تحويل الائتمان الألماني ISO 20022 كمثال.</span><span class="sxs-lookup"><span data-stu-id="42cb4-105">The German ISO 20022 credit transfer format is used as an example.</span></span> <span data-ttu-id="42cb4-106">يمكنك استخدام هذا الإجراء لتنسيقات التقارير الإلكترونية الأخرى المتوفرة.</span><span class="sxs-lookup"><span data-stu-id="42cb4-106">This procedure can be used for other available electronic reporting format.</span></span> 

<span data-ttu-id="42cb4-107">تم إنشاء هذه المهمة باستخدام شركة بيانات العرض التوضيحي DEMF، ولكن يمكنك استخدام أي من شركات بيانات العرض التوضيحي لإكمال هذه المهمة.</span><span class="sxs-lookup"><span data-stu-id="42cb4-107">This task was created using the demo data company DEMF but you can use any demo data company to complete this task.</span></span>

<span data-ttu-id="42cb4-108">هذه هي المهمة الأولى من ضمن خمس مهام، هدفها أن تعمل معًا على توضيح عملية معالجة مدفوعات المورّد باستخدام تكوينات التقارير الإلكترونية.</span><span class="sxs-lookup"><span data-stu-id="42cb4-108">This is the first of five tasks, that together illustrate the vendor payment process using electronic reporting configurations.</span></span> <span data-ttu-id="42cb4-109">يتم استخدام هذا الإجراء لميزة تمت إضافتها في Dynamics 365 for Operations، الإصدار 1611.</span><span class="sxs-lookup"><span data-stu-id="42cb4-109">This procedure is for a feature that was added in Dynamics 365 for Operations version 1611.</span></span>

1. <span data-ttu-id="42cb4-110">انتقل إلى إدارة المؤسسة > مساحات العمل‬ > إعداد التقارير الإلكتروني‬.</span><span class="sxs-lookup"><span data-stu-id="42cb4-110">Go to Organization administration > Workspaces > Electronic reporting.</span></span>
2. <span data-ttu-id="42cb4-111">في قائمة "موفرو التكوين‬" المتوفرون، حدد Microsoft.</span><span class="sxs-lookup"><span data-stu-id="42cb4-111">In the list of available configuration providers, select Microsoft.</span></span>
3. <span data-ttu-id="42cb4-112">انقر فوق "تعيين كنشط".</span><span class="sxs-lookup"><span data-stu-id="42cb4-112">Click Set active.</span></span>
4. <span data-ttu-id="42cb4-113">انقر فوق "المستودعات".</span><span class="sxs-lookup"><span data-stu-id="42cb4-113">Click Repositories.</span></span>
5. <span data-ttu-id="42cb4-114">انقر فوق "فتح".</span><span class="sxs-lookup"><span data-stu-id="42cb4-114">Click Open.</span></span>
6. <span data-ttu-id="42cb4-115">انقر فوق "إظهار عوامل التصفية".</span><span class="sxs-lookup"><span data-stu-id="42cb4-115">Click Show filters.</span></span>
7. <span data-ttu-id="42cb4-116">طبّق عوامل التصفية التالية: أدخل قيمة عامل التصفية "تحويل الائتمان ISO20022 (DE)" في حقل "اسم التكوين" باستخدام مشغل عامل التصفية "يبدأ بـ".</span><span class="sxs-lookup"><span data-stu-id="42cb4-116">Apply the following filters: Enter a filter value of "ISO20022 Credit transfer (DE)" on the "Configuration name" field using the "begins with" filter operator</span></span>
    * <span data-ttu-id="42cb4-117">أو، يمكنك العثور على التكوين في القائمة، وتحديده، ثم نقله إلى مهمة الاستيراد.</span><span class="sxs-lookup"><span data-stu-id="42cb4-117">Alternatively, you can find the configuration in the list, select it, and then move it to the Import task.</span></span>  
8. <span data-ttu-id="42cb4-118">انقر فوق "استيراد".</span><span class="sxs-lookup"><span data-stu-id="42cb4-118">Click Import.</span></span>
    * <span data-ttu-id="42cb4-119">إذا لم يتوفر الزر "استيراد"، فهذا يعني أن التكوين قد تم استيراده.</span><span class="sxs-lookup"><span data-stu-id="42cb4-119">If the Import button is not available, it means that the configuration has  already been imported.</span></span>  
9. <span data-ttu-id="42cb4-120">انقر فوق نعم.</span><span class="sxs-lookup"><span data-stu-id="42cb4-120">Click Yes.</span></span>

