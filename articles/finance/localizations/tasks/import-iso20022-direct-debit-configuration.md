---
title: استيراد تكوين الدين المباشر ISO20022
description: يوضح هذا الإجراء كيفية استيراد تكوين التقارير الإلكترونية لمدفوعات العميل.‬
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
ms.openlocfilehash: e5d4256b155d3e06d63e425fab63b4025ef2577f
ms.sourcegitcommit: 57e1dafa186fec77ddd8ba9425d238e36e0f0998
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 03/18/2020
ms.locfileid: "3140008"
---
# <a name="import-iso20022-direct-debit-configuration"></a><span data-ttu-id="0d21e-103">استيراد تكوين الدين المباشر ISO20022</span><span class="sxs-lookup"><span data-stu-id="0d21e-103">Import ISO20022 direct debit configuration</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="0d21e-104">يوضح هذا الإجراء كيفية استيراد تكوين التقارير الإلكترونية لمدفوعات العميل.‬</span><span class="sxs-lookup"><span data-stu-id="0d21e-104">This procedure demonstrates how to import a customer payment electronic reporting configuration.</span></span> <span data-ttu-id="0d21e-105">يستخدم هذا الإجراء تنسيق الدين المباشر ISO 20022 كمثال.</span><span class="sxs-lookup"><span data-stu-id="0d21e-105">This procedure uses the ISO 20022 direct debit format as an example.</span></span> 



<span data-ttu-id="0d21e-106">تم إنشاء هذا الإجراء باستخدام شركة بيانات العرض التوضيحي DEMF، ولكن يمكنك استخدام أي من شركات بيانات العرض التوضيحي لهذا الغرض.</span><span class="sxs-lookup"><span data-stu-id="0d21e-106">This procedure was created using the demo data company DEMF but you can use any demo data company for this purpose.</span></span>



<span data-ttu-id="0d21e-107">هذا هو الإجراء الأول من ضمن خمسة إجراءات هدفها توضيح عملية معالجة مدفوعات العميل باستخدام تكوينات التقارير الإلكترونية.</span><span class="sxs-lookup"><span data-stu-id="0d21e-107">This is the first of five procedures that demonstrate the customer payment process using electronic reporting configurations.</span></span>

1. <span data-ttu-id="0d21e-108">انتقل إلى إدارة المؤسسة > مساحات العمل‬ > إعداد التقارير الإلكتروني‬.</span><span class="sxs-lookup"><span data-stu-id="0d21e-108">Go to Organization administration > Workspaces > Electronic reporting.</span></span>
2. <span data-ttu-id="0d21e-109">في قائمة "موفرو التكوين‬" المتوفرون، حدد Microsoft.</span><span class="sxs-lookup"><span data-stu-id="0d21e-109">In the list of available configuration providers, select Microsoft.</span></span>
3. <span data-ttu-id="0d21e-110">انقر فوق "تعيين كنشط".</span><span class="sxs-lookup"><span data-stu-id="0d21e-110">Click Set active.</span></span>
4. <span data-ttu-id="0d21e-111">انقر فوق "المستودعات".</span><span class="sxs-lookup"><span data-stu-id="0d21e-111">Click Repositories.</span></span>
5. <span data-ttu-id="0d21e-112">انقر فوق "فتح".</span><span class="sxs-lookup"><span data-stu-id="0d21e-112">Click Open.</span></span>
6. <span data-ttu-id="0d21e-113">انقر فوق "إظهار عوامل التصفية".</span><span class="sxs-lookup"><span data-stu-id="0d21e-113">Click Show filters.</span></span>
7. <span data-ttu-id="0d21e-114">طبّق عوامل التصفية التالية: أدخل قيمة عامل التصفية "الدين المباشر ISO20022 (DE)" في حقل "اسم التكوين" باستخدام مشغل عامل التصفية "يبدأ بـ".</span><span class="sxs-lookup"><span data-stu-id="0d21e-114">Apply the following filters: Enter a filter value of "ISO20022 Direct debit (DE)" on the "Configuration name" field using the "begins with" filter operator</span></span>
    * <span data-ttu-id="0d21e-115">بشكل اختياري، يمكنك العثور على التكوين في القائمة، وتحديده ثم تخطي هذه الخطوة.</span><span class="sxs-lookup"><span data-stu-id="0d21e-115">Optionally, you can find the configuration in the list, select it, and skip this step.</span></span>  
8. <span data-ttu-id="0d21e-116">انقر فوق "استيراد".</span><span class="sxs-lookup"><span data-stu-id="0d21e-116">Click Import.</span></span>
    * <span data-ttu-id="0d21e-117">إذا لم يتوفر الزر "استيراد"، فهذا يعني أن التكوين قد تم استيراده.</span><span class="sxs-lookup"><span data-stu-id="0d21e-117">If the Import button is not available, it means that the configuration has been imported already.</span></span>  
9. <span data-ttu-id="0d21e-118">انقر فوق نعم.</span><span class="sxs-lookup"><span data-stu-id="0d21e-118">Click Yes.</span></span>

