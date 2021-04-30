---
title: نظرة عامة على تكامل Dynamics 365 Commerce وMicrosoft Teams
description: يقدم هذا الموضوع نظرة عامة على تكامل Microsoft Dynamics 365 Commerce وMicrosoft Teams.
author: gvrmohanreddy
manager: annbe
ms.date: 03/31/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.search.region: Global
ms.author: gmohanv
ms.search.validFrom: 2021-01-15
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: b9289aca4f53eb2ae8f1fa06d5f80b7ee0bbab8e
ms.sourcegitcommit: 34b478f175348d99df4f2f0c2f6c0c21b6b2660a
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 04/16/2021
ms.locfileid: "5908457"
---
# <a name="dynamics-365-commerce-and-microsoft-teams-integration-overview"></a><span data-ttu-id="62417-103">نظرة عامة على تكامل Dynamics 365 Commerce وMicrosoft Teams</span><span class="sxs-lookup"><span data-stu-id="62417-103">Dynamics 365 Commerce and Microsoft Teams integration overview</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="62417-104">يقدم هذا الموضوع نظرة عامة على تكامل Microsoft Dynamics 365 Commerce وMicrosoft Teams.</span><span class="sxs-lookup"><span data-stu-id="62417-104">This topic presents an overview of Microsoft Dynamics 365 Commerce and Microsoft Teams integration.</span></span>

<span data-ttu-id="62417-105">يتكامل Dynamics 365 Commerce مع Teams لمساعدة العملاء وموظفيهم على تحسين الإنتاجية من خلال مزامنة إدارة المهام بين التطبيقين.</span><span class="sxs-lookup"><span data-stu-id="62417-105">Dynamics 365 Commerce is integrating with Teams to help customers and their employees improve productivity by synchronizing task management between the two applications.</span></span> <span data-ttu-id="62417-106">تتيح إدارة المهام السلسة التي يوفرها تكامل Commerce وTeams لمديري المتاجر والموظفين إنشاء قوائم مهام، وتعيين المهام إلى متاجر متعددة، وتتبع حالة المهام عبر المتاجر، من أي تطبيق.</span><span class="sxs-lookup"><span data-stu-id="62417-106">The seamless task management that Commerce and Teams integration provides lets store managers and employees create task lists, assign tasks to multiple stores, and track the status of tasks across stores, from either application.</span></span>

<span data-ttu-id="62417-107">يتوفر تكامل Commerce وTeams اعتبارًا من إصدار Commerce رقم 10.0.18.</span><span class="sxs-lookup"><span data-stu-id="62417-107">Commerce and Teams integration is available as of the Commerce version 10.0.18 release.</span></span>

## <a name="key-features"></a><span data-ttu-id="62417-108">الميزات الرئيسية</span><span class="sxs-lookup"><span data-stu-id="62417-108">Key features</span></span>

<span data-ttu-id="62417-109">فيما يلي بعض الميزات الأساسية التي يوفرها تكامل Commerce وMicrosoft Teams:</span><span class="sxs-lookup"><span data-stu-id="62417-109">Here are some of the key features that the Commerce and Microsoft Teams integration provides:</span></span>

- <span data-ttu-id="62417-110">قم بتوفير Teams من خلال الاستفادة من المعلومات المحددة جيدًا من Commerce، مثل الهيكل التنظيمي والمعلومات حول المتاجر والعاملين والأذونات وسياق الأعمال.</span><span class="sxs-lookup"><span data-stu-id="62417-110">Provision Teams by taking advantage of well-defined information from Commerce, such as the organizational structure and information about stores, workers, permissions, and business context.</span></span>
- <span data-ttu-id="62417-111">قم بمزامنة التغييرات الجارية بسهولة (على سبيل المثال، إضافة متاجر جديدة أو تعيين موظفين جدد) بين Commerce وTeams، ولكن حافظ على Commerce كمصدر رئيسي لبيانات الهيكل التنظيمي.</span><span class="sxs-lookup"><span data-stu-id="62417-111">Easily synchronize ongoing changes (for example, the addition of new stores or hiring of new employees) between Commerce and Teams, but keep Commerce as the master source of organizational structure data.</span></span>
- <span data-ttu-id="62417-112">قم بدمج إدارة المهام بين Commerce وTeams لمساعدة عمال التخزين ومديري المتاجر والمديرين الإقليميين ومديري الاتصالات على إدارة المهام من أي تطبيق.</span><span class="sxs-lookup"><span data-stu-id="62417-112">Integrate task management between Commerce and Teams to help store workers, store managers, regional managers, and communications managers handle task management from either application.</span></span>

## <a name="prerequisites-for-using-integration-features"></a><span data-ttu-id="62417-113">المتطلبات الأساسية لاستخدام ميزات التكامل</span><span class="sxs-lookup"><span data-stu-id="62417-113">Prerequisites for using integration features</span></span>

<span data-ttu-id="62417-114">يجب أن تكون المتطلبات الأساسية التالية في مكانها قبل أن تتمكن من البدء في استخدام ميزات تكامل Microsoft Teams:</span><span class="sxs-lookup"><span data-stu-id="62417-114">The following prerequisites must be in place before you can start to use Microsoft Teams integration features:</span></span>

- <span data-ttu-id="62417-115">ترخيص Microsoft 365 Business Standard (يتضمن هذا الترخيص Teams.)</span><span class="sxs-lookup"><span data-stu-id="62417-115">Microsoft 365 Business Standard License (This license includes Teams.)</span></span>
- <span data-ttu-id="62417-116">حسابات Azure Active Directory (Azure AD) لجميع مديري المتاجر والعاملين</span><span class="sxs-lookup"><span data-stu-id="62417-116">Azure Active Directory (Azure AD) accounts for all store managers and workers</span></span>
- <span data-ttu-id="62417-117">أنظمة نقاط البيع (POS) التي تم تكوينها باستخدام مصادقة Azure AD</span><span class="sxs-lookup"><span data-stu-id="62417-117">Point of sale (POS) systems that are configured with Azure AD authentication</span></span>

## <a name="conceptual-architecture"></a><span data-ttu-id="62417-118">بنية تصورية</span><span class="sxs-lookup"><span data-stu-id="62417-118">Conceptual architecture</span></span>

<span data-ttu-id="62417-119">يبين الرسم التوضيحي التالي البنية التصورية لتكامل Dynamics 365 Commerce وMicrosoft Teams، باستخدام متجر سان فرانسيسكو كمثال.</span><span class="sxs-lookup"><span data-stu-id="62417-119">The following illustration shows the conceptual architecture of Dynamics 365 Commerce and Microsoft Teams integration, using a San Francisco store as an example.</span></span> <span data-ttu-id="62417-120">يقوم كل من Teams وتطبيق Commerce POS باستخدام Microsoft Planner كمستودع بحيث تظهر المهام المنشورة من Teams في تطبيق نقطة البيع وتظهر المهام المخصصة التي أنشأها مديرو المتجر في تطبيق نقطة البيع في Teams، مما يؤدي إلى تجربة إدارة مهام سلسة بين التطبيقات .</span><span class="sxs-lookup"><span data-stu-id="62417-120">Both Teams and the Commerce POS application use Microsoft Planner as a repository so that tasks published from Teams appear in the POS application and ad hoc tasks created by store managers in the POS application appear in Teams, resulting in a seamless task management experience between the applications.</span></span>    

![بنية تكامل Commerce وTeams](media/d365-commerce-teams-integration-conceptual-architecture.png)

## <a name="additional-resources"></a><span data-ttu-id="62417-122">الموارد الإضافية</span><span class="sxs-lookup"><span data-stu-id="62417-122">Additional resources</span></span>

[<span data-ttu-id="62417-123">تمكين تكامل Dynamics 365 Commerce وMicrosoft Teams</span><span class="sxs-lookup"><span data-stu-id="62417-123">Enable Dynamics 365 Commerce and Microsoft Teams integration</span></span>](enable-teams-integration.md)

[<span data-ttu-id="62417-124">توفير Microsoft Teams من Dynamics 365 Commerce</span><span class="sxs-lookup"><span data-stu-id="62417-124">Provision Microsoft Teams from Dynamics 365 Commerce</span></span>](provision-teams-from-commerce.md)

[<span data-ttu-id="62417-125">مزامنة إدارة المهام بين Microsoft Teams ونقطة بيع Dynamics 365 Commerce</span><span class="sxs-lookup"><span data-stu-id="62417-125">Synchronize task management between Microsoft Teams and Dynamics 365 Commerce POS</span></span>](synchronize-tasks-teams-pos.md)

[<span data-ttu-id="62417-126">إدارة أدوار المستخدمين في Microsoft Teams</span><span class="sxs-lookup"><span data-stu-id="62417-126">Manage user roles in Microsoft Teams</span></span>](manage-user-roles-teams.md)

[<span data-ttu-id="62417-127">تعيين المتاجر والفرق عند وجود فرق موجودة مسبقًا في Microsoft Teams</span><span class="sxs-lookup"><span data-stu-id="62417-127">Map stores and teams if there are pre-existing teams in Microsoft Teams</span></span>](map-stores-existing-teams.md)

[<span data-ttu-id="62417-128">الأسئلة الشائعة حول تكامل Dynamics 365 Commerce وMicrosoft Teams</span><span class="sxs-lookup"><span data-stu-id="62417-128">Dynamics 365 Commerce and Microsoft Teams integration FAQ</span></span>](teams-integration-faq.md)
