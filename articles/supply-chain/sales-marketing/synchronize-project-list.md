---
title: مزامنة قائمة المشاريع من Supply Chain Management إلى Field Service
description: يناقش هذا الموضوع القوالب والمهام الأساسية التي يتم استخدامها لمزامنة المشاريع من Dynamics 365 Supply Chain Management إلى Dynamics 365 Field Service.
author: ChristianRytt
manager: tfehr
ms.date: 03/13/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: crytt
ms.dyn365.ops.version: 8.1.3
ms.search.validFrom: 2018-12-01
ms.openlocfilehash: d80fce409ee92973a6134d96ce839b9722980918
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 04/02/2020
ms.locfileid: "3215920"
---
# <a name="synchronize-project-list-from-supply-chain-management-to-field-service"></a><span data-ttu-id="1adb0-103">مزامنة قائمة المشاريع من Supply Chain Management إلى Field Service</span><span class="sxs-lookup"><span data-stu-id="1adb0-103">Synchronize project list from Supply Chain Management to Field Service</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="1adb0-104">يناقش هذا الموضوع القوالب والمهام الأساسية التي يتم استخدامها لمزامنة المشاريع من Dynamics 365 Supply Chain Management إلى Dynamics 365 Field Service.</span><span class="sxs-lookup"><span data-stu-id="1adb0-104">This topic discusses the templates and underlying tasks that are used to synchronize projects from Dynamics 365 Supply Chain Management to Dynamics 365 Field Service.</span></span>

<span data-ttu-id="1adb0-105">[![مزامنة عمليات الأعمال بين Supply Chain Management وField Service](./media/FSProjectOW.png)](./media/FSProjectOW.png)</span><span class="sxs-lookup"><span data-stu-id="1adb0-105">[![Synchronization of business processes between Supply Chain Management and Field Service](./media/FSProjectOW.png)](./media/FSProjectOW.png)</span></span>

## <a name="templates-and-tasks"></a><span data-ttu-id="1adb0-106">القوالب والمهام</span><span class="sxs-lookup"><span data-stu-id="1adb0-106">Templates and tasks</span></span>
<span data-ttu-id="1adb0-107">يتم استخدام القوالب والمهام الأساسية التالية لتشغيل مزامنة المشاريع من Supply Chain Management إلى Field Service.</span><span class="sxs-lookup"><span data-stu-id="1adb0-107">The following template and underlying tasks are used to run synchronization of projects from Supply Chain Management to Field Service.</span></span>

<span data-ttu-id="1adb0-108">**قالب في تكامل البيانات**</span><span class="sxs-lookup"><span data-stu-id="1adb0-108">**Template in Data integration**</span></span>
- <span data-ttu-id="1adb0-109">المشاريع (Supply Chain Management إلى Field Service)</span><span class="sxs-lookup"><span data-stu-id="1adb0-109">Projects (Supply Chain Management to Field Service)</span></span>

<span data-ttu-id="1adb0-110">**مهمة في مشروع تكامل البيانات**</span><span class="sxs-lookup"><span data-stu-id="1adb0-110">**Task in the Data integration project**</span></span>
- <span data-ttu-id="1adb0-111">المشاريع</span><span class="sxs-lookup"><span data-stu-id="1adb0-111">Projects</span></span>

<span data-ttu-id="1adb0-112">يجب تنفيذ مهام المزامنة التالية قبل حدوث مزامنة مستويات قائمة المشاريع:</span><span class="sxs-lookup"><span data-stu-id="1adb0-112">The following synchronization tasks are required before synchronization of project list can occur:</span></span>
- <span data-ttu-id="1adb0-113">الحسابات (Sales إلى Supply Chain Management)</span><span class="sxs-lookup"><span data-stu-id="1adb0-113">Accounts (Sales to Supply Chain Management)</span></span> 

## <a name="entity-set"></a><span data-ttu-id="1adb0-114">مجموعة الكيانات</span><span class="sxs-lookup"><span data-stu-id="1adb0-114">Entity set</span></span>
| <span data-ttu-id="1adb0-115">Field Service</span><span class="sxs-lookup"><span data-stu-id="1adb0-115">Field Service</span></span>           | <span data-ttu-id="1adb0-116">Supply Chain Management</span><span class="sxs-lookup"><span data-stu-id="1adb0-116">Supply Chain Management</span></span>  |
|-------------------------|-------------------------|
|<span data-ttu-id="1adb0-117">msdynce_externalprojects</span><span class="sxs-lookup"><span data-stu-id="1adb0-117">msdynce_externalprojects</span></span> | <span data-ttu-id="1adb0-118">المشاريع</span><span class="sxs-lookup"><span data-stu-id="1adb0-118">Projects</span></span>                |

## <a name="entity-flow"></a><span data-ttu-id="1adb0-119">تدفق الكيان</span><span class="sxs-lookup"><span data-stu-id="1adb0-119">Entity flow</span></span>
<span data-ttu-id="1adb0-120">يتم إنشاء المشاريع في Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="1adb0-120">Projects are created in Supply Chain Management.</span></span> <span data-ttu-id="1adb0-121">ستتم مزامنة المشاريع التي تم فيها تعيين **نوع المشروع** إلى **الوقت والمادة** وتعيين **مرحلة المشروع** إلى **قيد التقدم** مع الكيان **مشروع خارجي** في Field Service، بما في ذلك رقم المشروع واسم المشروع ومرحلة المشروع ومعلومات حساب العميل.</span><span class="sxs-lookup"><span data-stu-id="1adb0-121">Projects with **Project type** set to **Time and material** and **Project stage** set to **In process** will synchronize to the **External Project** entity in Field Service, including Project number, Project name, Project stage, and Customer account information.</span></span> <span data-ttu-id="1adb0-122">تُستخدم قائمة **المشروع الخارجي** لإقران أوامر عمل Field service مع مشاريع Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="1adb0-122">The **External Project** list is used to pair Field service work orders with Supply Chain Management projects.</span></span>

## <a name="field-service-crm-solution"></a><span data-ttu-id="1adb0-123">حل Field Service CRM</span><span class="sxs-lookup"><span data-stu-id="1adb0-123">Field Service CRM solution</span></span>
<span data-ttu-id="1adb0-124">يحصل الكيان **مشروع الخارجي** على جميع المشاريع من Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="1adb0-124">The **External Project** entity gets all the projects from Supply Chain Management.</span></span> <span data-ttu-id="1adb0-125">تمت إضافة الحقل **مشروع خارجي** إلى الكيان **أمر عمل**.</span><span class="sxs-lookup"><span data-stu-id="1adb0-125">The **External Project** field has been added to the **Work Order** entity.</span></span> <span data-ttu-id="1adb0-126">هذا الحقل عبارة عن حقل بحث، ومن خلال وضع علامة على أمر العمل بواسطة مشروع، يتم عندئذٍ توصيل أمر المبيعات بمشروع ضمن Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="1adb0-126">This is a lookup field, so by tagging your work order with a project, the sales order will be connected to a project within Supply Chain Management.</span></span> <span data-ttu-id="1adb0-127">عندما تتغير **حالة النظام** من **مفتوح – قيد التقدم(690,970,000)** إلى حالة أعلى، سيتم تأمين الحقل **مشروع خارجي** وسيتعذر عليك إضافة القيمة أو إزالتها أو تغييرها.</span><span class="sxs-lookup"><span data-stu-id="1adb0-127">After the **System Status** changes **Open – In Progress(690,970,000)** to a higher status, the **External Project** field will be locked and you can no longer add, remove, or change the value.</span></span>

## <a name="prerequisites-and-mapping-setup"></a><span data-ttu-id="1adb0-128">المتطلبات الأساسية وإعداد التعيين</span><span class="sxs-lookup"><span data-stu-id="1adb0-128">Prerequisites and mapping setup</span></span>
### <a name="supply-chain-management"></a><span data-ttu-id="1adb0-129">Supply Chain Management</span><span class="sxs-lookup"><span data-stu-id="1adb0-129">Supply Chain Management</span></span>
<span data-ttu-id="1adb0-130">تمكين تعقب التغييرات لمشاريع كيان البيانات.</span><span class="sxs-lookup"><span data-stu-id="1adb0-130">Enable change tracking for Data entity projects.</span></span>

## <a name="template-mapping-in-data-integration"></a><span data-ttu-id="1adb0-131">تعيين القالب في تكامل البيانات</span><span class="sxs-lookup"><span data-stu-id="1adb0-131">Template mapping in Data integration</span></span>


### <a name="projects-supply-chain-management-to-field-service-projects"></a><span data-ttu-id="1adb0-132">المشاريع (Supply Chain Management إلى Field Service): المشاريع</span><span class="sxs-lookup"><span data-stu-id="1adb0-132">Projects (Supply Chain Management to Field Service): Projects</span></span>

<span data-ttu-id="1adb0-133">[![تعيين القالب في تكامل البيانات](./media/FSProject1.png)](./media/FSProject1.png)</span><span class="sxs-lookup"><span data-stu-id="1adb0-133">[![Template mapping in Data integration](./media/FSProject1.png)](./media/FSProject1.png)</span></span>
