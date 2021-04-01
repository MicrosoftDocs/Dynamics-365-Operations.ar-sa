---
title: طريقة عرض الأصول
description: يصف هذا الموضوع طريقة عرض الأصول في إدارة الأصول.
author: josaw1
manager: tfehr
ms.date: 06/26/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CatProcureCatalogEdit, CatProcureCatalogListPage, EntAssetObjectTree, EntAssetFunctionalLocationTree
audience: Application User
ms.reviewer: kamaybac
ms.custom: 2214
ms.assetid: 2f3e0441-414d-402b-b28b-7ab0d650d658
ms.search.region: Global
ms.author: riluan
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 2a770831c564d44de534642cc462b27b0818e9a2
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 02/15/2021
ms.locfileid: "5253100"
---
# <a name="asset-view"></a><span data-ttu-id="ce484-103">طريقة عرض الأصول</span><span class="sxs-lookup"><span data-stu-id="ce484-103">Asset view</span></span>

[!include [banner](../../includes/banner.md)]

 

<span data-ttu-id="ce484-104">يصف هذا الموضوع طريقة عرض الأصول في إدارة الأصول.</span><span class="sxs-lookup"><span data-stu-id="ce484-104">This topic describes the asset view in Asset Management.</span></span> <span data-ttu-id="ce484-105">تعرض صفحة **طريقة عرض الأصول** الأصول النشطة ومواقع العمل في طريقة عرض شجرة.</span><span class="sxs-lookup"><span data-stu-id="ce484-105">The **Asset view** page shows active assets and functional locations in a tree view.</span></span> <span data-ttu-id="ce484-106">وبالتالي، يمكنك أن تحصل بسهولة على نظرة عامة على علاقات الأصول بمواقع العمل.</span><span class="sxs-lookup"><span data-stu-id="ce484-106">Therefore, you can easily get an overview of asset relations to functional locations.</span></span> <span data-ttu-id="ce484-107">بالإضافة إلى ذلك، يمكنك عرض معلومات مفصلة حول مواقع العمل والأصول وقوائم مكونات الصنف (BOM) ذات الصلة.</span><span class="sxs-lookup"><span data-stu-id="ce484-107">Additionally, you can view detailed information about functional locations, assets, and related bills of materials (BOMs).</span></span> <span data-ttu-id="ce484-108">يمكنك أيضًا الحصول على نظرة عامة سريعة على طلبات الصيانة النشطة وأوامر العمل المرتبطة بأصل ما.</span><span class="sxs-lookup"><span data-stu-id="ce484-108">You can also get a quick overview of active maintenance requests and work orders that are related to an asset.</span></span>

1. <span data-ttu-id="ce484-109">حدد **إدارة الأصول** \> **عام** \> **الأصول** \> **طريقة عرض الأصول‏‎**.</span><span class="sxs-lookup"><span data-stu-id="ce484-109">Select **Asset management** \> **Common** \> **Assets** \> **Asset view**.</span></span>
2. <span data-ttu-id="ce484-110">لتغيير طريقة العرض المعروضة في الصفحة، حدد قيمة جديدة في حقل **طريقة العرض**.</span><span class="sxs-lookup"><span data-stu-id="ce484-110">To change the view that is shown on the page, select a new value in the **View** field.</span></span>

    > [!NOTE]
    > <span data-ttu-id="ce484-111">تتوقف طريقة العرض الافتراضية التي تظهر عندما تفتح صفحة **طريقة عرض الأصول** على القيمة المحددة في حقل **طريقة العرض** على علامة تبويب **الأصول** في صفحة **معلمات إدارة الأصول** (**إدارة الأصول** \> **الإعداد** \> **معلمات إدارة الأصول**).</span><span class="sxs-lookup"><span data-stu-id="ce484-111">The default view that is shown when you open the **Asset view** page depends on the value that is selected in the **View** field on the **Assets** tab of the **Asset management parameters** page (**Asset management** \> **Setup** \> **Asset management parameters**).</span></span>

<span data-ttu-id="ce484-112">على الجانب الأيسر من الصفحة، تعرض علامات التبويب السريعة تفاصيل طريقة العرض المحددة.</span><span class="sxs-lookup"><span data-stu-id="ce484-112">On the right side of the page, FastTabs shows details of the selected view.</span></span>

<span data-ttu-id="ce484-113">يعرض مسار العنوان الذي يظهر أعلى طريقة عرض الشجرة التحديد الحالي في طريقة عرض الشجرة.</span><span class="sxs-lookup"><span data-stu-id="ce484-113">The breadcrumb trail that appears above the tree view shows the current selection in the tree view.</span></span> <span data-ttu-id="ce484-114">يستخدم مسار العنوان هذا التنسيق التالي:</span><span class="sxs-lookup"><span data-stu-id="ce484-114">This breadcrumb trail uses the following format:</span></span>

<span data-ttu-id="ce484-115">معرف موقع العمل / معرف موقع العمل (عند وجود أكثر من موقع عمل واحد) \> معرف الأصل / معرف الأصل (عند وجود أكثر من معرف أصل واحد) - رقم الصنف.</span><span class="sxs-lookup"><span data-stu-id="ce484-115">Functional location ID / Functional location ID (if there is more than one functional location) \> Asset ID / Asset ID (if there is more than one asset) - Item number.</span></span>

<span data-ttu-id="ce484-116">إذا قمت بتحديد أصل في طريقة عرض الشجرة، فيمكنك تحديد **الطلبات النشطة** أو **أوامر العمل النشطة** لعرض طلبات الصيانة أو أوامر العمل المرتبطة بالأصل.</span><span class="sxs-lookup"><span data-stu-id="ce484-116">If you've selected an asset in the tree view, you can select **Active requests** or **Active work orders** to view the maintenance requests or work orders that are related to the asset.</span></span> <span data-ttu-id="ce484-117">يمكنك أيضًا تحديد **فتح** \> **موقع العمل** أو **الأصل** أو **BOM‏‎ الأصل** لفتح طريقة العرض ذات الصلة.</span><span class="sxs-lookup"><span data-stu-id="ce484-117">You can also select **Open** \> **Functional location**, **Asset**, or **Asset BOM** to open the related view.</span></span>

<span data-ttu-id="ce484-118">يتوفر أيضًا خيار **مواقع عمل الأصل** الذي يمكنك تحديده في حقل **طريقة العرض** في أي بحث عن الأصول حيث يمكنك تحديد أصل.</span><span class="sxs-lookup"><span data-stu-id="ce484-118">The **Asset functional locations** option that you can select in the **View** field is also available in any asset lookup where you can select an asset.</span></span> <span data-ttu-id="ce484-119">تظهر طريقة عرض الشجرة على علامة التبويب **طريقة عرض الأصول**، على سبيل المثال، حيث يمكنك [إنشاء أصل](../objects/create-an-object.md) أو إنشاء طلب صيانة أو إنشاء أمر عمل.</span><span class="sxs-lookup"><span data-stu-id="ce484-119">The tree view is shown on an **Asset view** tab, for example, where you [create an asset](../objects/create-an-object.md), create a maintenance request, or create a work order.</span></span>


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]