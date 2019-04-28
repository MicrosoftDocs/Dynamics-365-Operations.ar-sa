---
title: أوامر مبيعات المشروع
description: يشرح هذا الموضوع كيفية إنشاء أوامر مبيعات قائمة على المشروع لمشاريع الوقت والمادة.
author: KimANelson
manager: AnnBe
ms.date: 04/05/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 87983
ms.assetid: b454ad57-2fd6-46c9-a77e-646de4153067
ms.search.region: Global
ms.author: knelson
ms.search.validFrom: 2019-04-05
ms.dyn365.ops.version: AX 10.0.2
ms.openlocfilehash: 1d54c98a08dc7cccb5cafbbe401d0ce25a276c25
ms.sourcegitcommit: 9796d022a8abf5c07abcdee6852ee34f06d2eb57
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 04/12/2019
ms.locfileid: "976624"
---
# <a name="project-sales-orders-for-time-and-material-projects"></a><span data-ttu-id="396d2-103">أوامر مبيعات المشروع لمشاريع الوقت والمادة</span><span class="sxs-lookup"><span data-stu-id="396d2-103">Project sales orders for time and material projects</span></span>

[!include[banner](../includes/banner.md)]
[!include[banner](../includes/preview-banner.md)]

<span data-ttu-id="396d2-104">يصف هذا الموضوع كيفية إنشاء أمر مبيعات لمشروع.</span><span class="sxs-lookup"><span data-stu-id="396d2-104">This topic describes how to create a sales order for a project.</span></span> <span data-ttu-id="396d2-105">يمكن إنشاء أوامر المبيعات فقط المشاريع من النوع **الوقت والمادة**.</span><span class="sxs-lookup"><span data-stu-id="396d2-105">Sales orders can only be created for projects of type **time and material**.</span></span>

<span data-ttu-id="396d2-106">إذا تضمن مشروع وقت ومادة مصادر تمويل متعددة في عقد المشروع، فيجب تمكين المحددة **السماح لأوامر مبيعات المشروعات مع مصادر تمويل متعددة‬** في صفحة **محددات إدارة المشاريع ومحاسبتها‬**.</span><span class="sxs-lookup"><span data-stu-id="396d2-106">If a time and material project has multiple funding sources on the project contract, you must enable the **Allow sales orders for projects with multiple funding sources** parameter on the **Project management and accounting parameters** page.</span></span> 

> [!NOTE]
> - <span data-ttu-id="396d2-107">يتوفر الدعم لأوامر مبيعات المشروع مع مصادر تمويل متعددة متوفرة اعتبارًا من إصدار التطبيق 10.0.2 والإصدارات اللاحقة.</span><span class="sxs-lookup"><span data-stu-id="396d2-107">Support for project sales orders with multiple funding sources is available starting with application release 10.0.2 and higher.</span></span>
> - <span data-ttu-id="396d2-108">في موجة إصدار أبريل 2020، ستُزال المحددة لتمكين الدعم لأوامر مبيعات المشروع الذي يتضمن مصادر تمويل متعددة، وبعد ذلك ستكون الوظيفة ممكّنة بشكل دائم.</span><span class="sxs-lookup"><span data-stu-id="396d2-108">The parameter to enable the support for project sales orders with multiple funding sources will be removed in the April 2020 release wave, after which the functionality will always be enabled.</span></span>

<span data-ttu-id="396d2-109">يمكنك إنشاء أوامر مبيعات قائمة على المشروع باستخدام طريقتين:</span><span class="sxs-lookup"><span data-stu-id="396d2-109">You can create project-based sales orders in two ways:</span></span>

- <span data-ttu-id="396d2-110">انتقل إلى المشروع بحد ذاته.</span><span class="sxs-lookup"><span data-stu-id="396d2-110">Go to the project itself.</span></span> <span data-ttu-id="396d2-111">في "جزء الإجراءات"، حدد **إدارة > عناصر المهام > أمر مبيعات**.</span><span class="sxs-lookup"><span data-stu-id="396d2-111">On the Action Pane, select **Manage > Item tasks > Sales order**.</span></span> <span data-ttu-id="396d2-112">ستكون معلومات المشروع الافتراضية أمر المبيعات من المشروع.</span><span class="sxs-lookup"><span data-stu-id="396d2-112">The project information will default to the sales order from the project.</span></span> <span data-ttu-id="396d2-113">إذا تضمن عقد المشروع أكثر من مصدر تمويل واحد، فستحتاج إلى تحديد مصدر التمويل لتعيين العميل لأمر المبيعات.</span><span class="sxs-lookup"><span data-stu-id="396d2-113">If the project contract has more than one funding source, you will need to select the funding source to set the customer for the sales order.</span></span> <span data-ttu-id="396d2-114">إذا كان هناك مصدر تمويل واحد فقط للمشروع، فسيتم تعيين العميل تلقائيًا.</span><span class="sxs-lookup"><span data-stu-id="396d2-114">If there is only one funding source for the project, the customer will be automatically set.</span></span>
- <span data-ttu-id="396d2-115">انتقل إلى صفحة قائمة **كافة أوامر المبيعات** وأنشئ أمر مبيعات جديدًا.</span><span class="sxs-lookup"><span data-stu-id="396d2-115">Go to the **All sales order** list page and create a new sales order.</span></span> <span data-ttu-id="396d2-116">ستحتاج إلى تحديد المشروع لأمر المبيعات.</span><span class="sxs-lookup"><span data-stu-id="396d2-116">You will need to select the project for the sales order.</span></span> <span data-ttu-id="396d2-117">بعد تحديد المشروع، سيتم تعيين العميل من مصدر التمويل أو ستحتاج إلى تحديد مصدر التمويل إذا تضمن عقد المشروع مصادر تمويل متعددة.</span><span class="sxs-lookup"><span data-stu-id="396d2-117">After the project is selected, the customer will be set from the funding source or you will need to select the funding source if the project contract has multiple funding sources.</span></span>

