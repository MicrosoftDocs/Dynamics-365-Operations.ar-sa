---
title: مجموعات حسابات توحيد وحسابات توحيد إضافية
description: يقدم هذا الموضوع معلومات حول مجموعات حسابات التوحيد وحسابات التوحيد الإضافية ويشرح كيفية استخدامها في Microsoft Dynamics 365 Finance.
author: aprilolson
manager: AnnBe
ms.date: 01/11/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LedgerConsolidateAccountGroup
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 265544
ms.assetid: 71c31df7-b655-46a8-8844-4f92a8bd71b0
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: 8db7a60656434aafd8114b08c2c0e9493140f27b
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 09/27/2019
ms.locfileid: "2176260"
---
# <a name="consolidation-account-groups-and-additional-consolidation-accounts"></a><span data-ttu-id="35076-103">مجموعات حسابات توحيد وحسابات توحيد إضافية</span><span class="sxs-lookup"><span data-stu-id="35076-103">Consolidation account groups and additional consolidation accounts</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="35076-104">يقدم هذا الموضوع معلومات حول مجموعات حسابات التوحيد وحسابات التوحيد الإضافية ويشرح كيفية استخدامها في Microsoft Dynamics 365 Finance.</span><span class="sxs-lookup"><span data-stu-id="35076-104">This topic provides information about consolidation account groups and additional consolidation accounts, and explains how they are used in Microsoft Dynamics 365 Finance.</span></span>

<a name="consolidation-account-groups"></a><span data-ttu-id="35076-105">مجموعات حسابات التوحيد</span><span class="sxs-lookup"><span data-stu-id="35076-105">Consolidation account groups</span></span>
----------------------------

<span data-ttu-id="35076-106">تتيح لك مجموعات حسابات التوحيد إنشاء مجموعات من الحسابات التي تريد استخدامها لتوحيد البيانات.</span><span class="sxs-lookup"><span data-stu-id="35076-106">Consolidation account groups let you create groups of the accounts that you want to use to consolidate data.</span></span> <span data-ttu-id="35076-107">في معظم الأحيان، تمثل مجموعة حسابات التوحيد مخطط حسابات حكومي أو تعيِّن الحسابات إلى مجموعة يتم تحديدها من قِبل المقر الرئيسي للشركة.</span><span class="sxs-lookup"><span data-stu-id="35076-107">Most often, a consolidation account group represents a government-mandated chart of accounts or maps accounts to a group that is defined by the company's headquarters.</span></span> <span data-ttu-id="35076-108">يمكنك العثور على مجموعات حسابات التوحيد في جزء **الإعداد** بالوحدة النمطية **عمليات التوحيد**.</span><span class="sxs-lookup"><span data-stu-id="35076-108">You can find consolidation account groups in the **Setup** area of the **Consolidations** module.</span></span> <span data-ttu-id="35076-109">عندما تقوم بإضافة مجموعة جديدة، أدخل معرفاً فريداً لمجموعة الحسابات واسمًا لها.</span><span class="sxs-lookup"><span data-stu-id="35076-109">When you add a new group, you enter a unique identifier for the account group and a name.</span></span>

## <a name="additional-consolidation-accounts"></a><span data-ttu-id="35076-110">حسابات التوحيد الإضافية</span><span class="sxs-lookup"><span data-stu-id="35076-110">Additional consolidation accounts</span></span>
<span data-ttu-id="35076-111">تتيح لك ‏‫حسابات التوحيد الإضافية‬ تعيين حساب من مخطط حسابات موجود إلى إحدى مجموعات حسابات التوحيد.</span><span class="sxs-lookup"><span data-stu-id="35076-111">Additional consolidation accounts let you assign an account from an existing chart of accounts to a consolidation account group.</span></span> <span data-ttu-id="35076-112">يمكنك بعد ذلك تحديد قيمة حساب التوحيد واسمه.</span><span class="sxs-lookup"><span data-stu-id="35076-112">You can then specify a consolidation account value and name.</span></span> 

<span data-ttu-id="35076-113">يمكنك العثور على حسابات التوحيد الإضافية في جزء **الإعداد** بالوحدة النمطية **عمليات التوحيد**.</span><span class="sxs-lookup"><span data-stu-id="35076-113">You can find additional consolidation accounts in the **Setup** area of the **Consolidations** module.</span></span> <span data-ttu-id="35076-114">عند إنشاء حساب توحيد جديد، يجب تحديد المعلومات التالية:</span><span class="sxs-lookup"><span data-stu-id="35076-114">When you create a new consolidation account, you must specify the following information:</span></span>

-   <span data-ttu-id="35076-115">**الحساب الرئيسي** – يعتبر هذا الحقل هو حقل بحث يوضح كافة الحسابات الرئيسية التي تستند إلى مخطط الحسابات الذي قمت بتحديده في الصفحة.</span><span class="sxs-lookup"><span data-stu-id="35076-115">**Main account** – This field is a lookup that shows all the main accounts that are based on the chart of accounts that you selected on the page.</span></span> <span data-ttu-id="35076-116">عند تحديد حساب، يتم تلقائياً إدخال الاسم في الحقل **اسم الحساب الرئيسي**.</span><span class="sxs-lookup"><span data-stu-id="35076-116">When you select an account, the name is automatically entered in the **Main account name** field.</span></span>
-   <span data-ttu-id="35076-117">**مجموعة حسابات التوحيد** – استخدم هذا الحقل لتحديد المجموعة لتعيين الحساب إليها.</span><span class="sxs-lookup"><span data-stu-id="35076-117">**Consolidation account group** – Use this field to specify the group to assign the account to.</span></span> <span data-ttu-id="35076-118">إذا أجريت التوحيد بطريقتين مختلفتين، يجب إضافة نفس الحساب لكافة مجموعات حسابات التوحيد الأربع.</span><span class="sxs-lookup"><span data-stu-id="35076-118">If you consolidate in two different ways, you must add the same account to all four consolidation account groups.</span></span>
-   <span data-ttu-id="35076-119">**حساب التوحيد** - أدخل قيمة حساب التوحيد.</span><span class="sxs-lookup"><span data-stu-id="35076-119">**Consolidation account** – Enter the value of the consolidation account.</span></span> <span data-ttu-id="35076-120">وهذه القيمة لا يلزم أن تكون حساباً من مخطط حسابات.</span><span class="sxs-lookup"><span data-stu-id="35076-120">This value doesn't have to be an account from a chart of accounts.</span></span> <span data-ttu-id="35076-121">يمكن أن تكون أي قيمة تتطلبها.</span><span class="sxs-lookup"><span data-stu-id="35076-121">It can be any value that you require.</span></span>
-   <span data-ttu-id="35076-122">**اسم حساب التوحيد** – أدخل اسم الحساب كما تريده أن يظهر في الاستعلامات والتقارير.</span><span class="sxs-lookup"><span data-stu-id="35076-122">**Consolidation account name** – Enter the name of account as you want it to appear on inquiries and reports.</span></span>
-   <span data-ttu-id="35076-123">**مستوى SAT** – يُستخدم هذا الحقل لإعداد تقارير بخصوص كشوف الحسابات لهيئات الضرائب المكسيكية.</span><span class="sxs-lookup"><span data-stu-id="35076-123">**SAT level** – This field is used to report account statements to the Mexican tax authorities.</span></span> 

<span data-ttu-id="35076-124">عند الانتهاء من إنشاء مجموعات حسابات التوحيد وحسابات التوحيد الإضافية، يمكنك تحديد المجموعة في عملية التوحيد عبر الإنترنت.</span><span class="sxs-lookup"><span data-stu-id="35076-124">When you've finished creating your consolidation account groups and additional consolidation accounts, you can select the group in the Consolidate online process.</span></span>


<span data-ttu-id="35076-125">لمزيد من المعلومات، راجع [إنشاء مجموعات توحيد وحسابات توحيد إضافية](../general-ledger/tasks/create-consolidation-groups.md).</span><span class="sxs-lookup"><span data-stu-id="35076-125">For more information, see [Create consolidation groups and additional consolidation accounts](../general-ledger/tasks/create-consolidation-groups.md).</span></span> 


