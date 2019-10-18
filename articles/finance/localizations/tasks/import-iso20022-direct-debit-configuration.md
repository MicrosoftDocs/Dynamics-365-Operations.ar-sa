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
ms.openlocfilehash: 7eee00021f49ac0110d7bde07faba8095348e1b4
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 09/27/2019
ms.locfileid: "2185740"
---
# <a name="import-iso20022-direct-debit-configuration"></a><span data-ttu-id="d89ed-103">استيراد تكوين الدين المباشر ISO20022</span><span class="sxs-lookup"><span data-stu-id="d89ed-103">Import ISO20022 direct debit configuration</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="d89ed-104">يوضح هذا الإجراء كيفية استيراد تكوين التقارير الإلكترونية لمدفوعات العميل.‬</span><span class="sxs-lookup"><span data-stu-id="d89ed-104">This procedure demonstrates how to import a customer payment electronic reporting configuration.</span></span> <span data-ttu-id="d89ed-105">يستخدم هذا الإجراء تنسيق الدين المباشر ISO 20022 كمثال.</span><span class="sxs-lookup"><span data-stu-id="d89ed-105">This procedure uses the ISO 20022 direct debit format as an example.</span></span> 



<span data-ttu-id="d89ed-106">تم إنشاء هذا الإجراء باستخدام شركة بيانات العرض التوضيحي DEMF، ولكن يمكنك استخدام أي من شركات بيانات العرض التوضيحي لهذا الغرض.</span><span class="sxs-lookup"><span data-stu-id="d89ed-106">This procedure was created using the demo data company DEMF but you can use any demo data company for this purpose.</span></span>



<span data-ttu-id="d89ed-107">هذا هو الإجراء الأول من ضمن خمسة إجراءات هدفها توضيح عملية معالجة مدفوعات العميل باستخدام تكوينات التقارير الإلكترونية.</span><span class="sxs-lookup"><span data-stu-id="d89ed-107">This is the first of five procedures that demonstrate the customer payment process using electronic reporting configurations.</span></span>

1. <span data-ttu-id="d89ed-108">انتقل إلى إدارة المؤسسة > مساحات العمل‬ > إعداد التقارير الإلكتروني‬.</span><span class="sxs-lookup"><span data-stu-id="d89ed-108">Go to Organization administration > Workspaces > Electronic reporting.</span></span>
2. <span data-ttu-id="d89ed-109">في قائمة "موفرو التكوين‬" المتوفرون، حدد Microsoft.</span><span class="sxs-lookup"><span data-stu-id="d89ed-109">In the list of available configuration providers, select Microsoft.</span></span>
3. <span data-ttu-id="d89ed-110">انقر فوق "تعيين كنشط".</span><span class="sxs-lookup"><span data-stu-id="d89ed-110">Click Set active.</span></span>
4. <span data-ttu-id="d89ed-111">انقر فوق "المستودعات".</span><span class="sxs-lookup"><span data-stu-id="d89ed-111">Click Repositories.</span></span>
5. <span data-ttu-id="d89ed-112">انقر فوق "فتح".</span><span class="sxs-lookup"><span data-stu-id="d89ed-112">Click Open.</span></span>
6. <span data-ttu-id="d89ed-113">انقر فوق "إظهار عوامل التصفية".</span><span class="sxs-lookup"><span data-stu-id="d89ed-113">Click Show filters.</span></span>
7. <span data-ttu-id="d89ed-114">طبّق عوامل التصفية التالية: أدخل قيمة عامل التصفية "الدين المباشر ISO20022 (DE)" في حقل "اسم التكوين" باستخدام مشغل عامل التصفية "يبدأ بـ".</span><span class="sxs-lookup"><span data-stu-id="d89ed-114">Apply the following filters: Enter a filter value of "ISO20022 Direct debit (DE)" on the "Configuration name" field using the "begins with" filter operator</span></span>
    * <span data-ttu-id="d89ed-115">بشكل اختياري، يمكنك العثور على التكوين في القائمة، وتحديده ثم تخطي هذه الخطوة.</span><span class="sxs-lookup"><span data-stu-id="d89ed-115">Optionally, you can find the configuration in the list, select it, and skip this step.</span></span>  
8. <span data-ttu-id="d89ed-116">انقر فوق "استيراد".</span><span class="sxs-lookup"><span data-stu-id="d89ed-116">Click Import.</span></span>
    * <span data-ttu-id="d89ed-117">إذا لم يتوفر الزر "استيراد"، فهذا يعني أن التكوين قد تم استيراده.</span><span class="sxs-lookup"><span data-stu-id="d89ed-117">If the Import button is not available, it means that the configuration has been imported already.</span></span>  
9. <span data-ttu-id="d89ed-118">انقر فوق نعم.</span><span class="sxs-lookup"><span data-stu-id="d89ed-118">Click Yes.</span></span>

