---
title: إضافة عملية حسابية إلى نموذج تكوين منتج
description: يوضح هذا الإجراء كيفية إضافة عملية حساب جديدة إلى نموذج تكوين منتج.
author: ShylaThompson
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: DefaultDashboard, EcoResProductVariantMaintainWorkspace, PCProductConfigurationModelListPage, PCProductConfigurationModelDetails, PCConstraintEditor, PCRuntimeConfiguratorValidate
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: e703c6d505f1e2e77f454732301de7a6c130c58a
ms.sourcegitcommit: 708ca25687a4e48271cdcd6d2d22d99fb94cf140
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 10/10/2020
ms.locfileid: "3986493"
---
# <a name="add-a-calculation-to-a-product-configuration-model"></a><span data-ttu-id="bef98-103">إضافة عملية حسابية إلى نموذج تكوين منتج</span><span class="sxs-lookup"><span data-stu-id="bef98-103">Add a calculation to a product configuration model</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="bef98-104">يوضح هذا الإجراء كيفية إضافة عملية حساب جديدة إلى نموذج تكوين منتج.</span><span class="sxs-lookup"><span data-stu-id="bef98-104">This procedure shows how to add a new calculation to a product configuration model.</span></span> <span data-ttu-id="bef98-105">ويُظهر كيف يمكنك إنشاء تعبير منطقي باستخدام العامل "لو" لتعيين ارتفاع مكبر الصوت إلى 10 لمكبرات الصوت البيضاء و15 لألوان الكابينات الأخرى.</span><span class="sxs-lookup"><span data-stu-id="bef98-105">It shows how you can create a logical expression using the "If" operator to set a speaker height to 10 for white speakers and 15 for all other cabinet finishes.</span></span> <span data-ttu-id="bef98-106">يستخدم الإجراء المكون مكبر الصوت المتطور في شركة العرض التوضيحي USMF.</span><span class="sxs-lookup"><span data-stu-id="bef98-106">The procedure uses the High end speaker component in the demo company USMF.</span></span>


## <a name="add-a-calculation"></a><span data-ttu-id="bef98-107">إضافة عملية حساب</span><span class="sxs-lookup"><span data-stu-id="bef98-107">Add a calculation</span></span>

## <a name="create-calculation-expression"></a><span data-ttu-id="bef98-108">إنشاء عملية تعبير حساب</span><span class="sxs-lookup"><span data-stu-id="bef98-108">Create calculation expression</span></span>
1. <span data-ttu-id="bef98-109">انقر فوق "تحرير التعبير".</span><span class="sxs-lookup"><span data-stu-id="bef98-109">Click Edit expression.</span></span>
2. <span data-ttu-id="bef98-110">في الحقل "ConstraintBody"، أدخل "If[CabinetFinish=="White", 10, 15]".</span><span class="sxs-lookup"><span data-stu-id="bef98-110">In the ConstraintBody field, enter 'If[CabinetFinish=="White", 10, 15]'.</span></span>
3. <span data-ttu-id="bef98-111">انقر فوق "التحقق من الصحة‬".</span><span class="sxs-lookup"><span data-stu-id="bef98-111">Click Validate.</span></span>
4. <span data-ttu-id="bef98-112">انقر فوق "إغلاق".</span><span class="sxs-lookup"><span data-stu-id="bef98-112">Click Close.</span></span>
5. <span data-ttu-id="bef98-113">انقر فوق "موافق".</span><span class="sxs-lookup"><span data-stu-id="bef98-113">Click OK.</span></span>

