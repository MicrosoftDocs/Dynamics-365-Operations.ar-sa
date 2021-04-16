---
title: تمكين تكامل Dynamics 365 Commerce وMicrosoft Teams
description: يوضح هذا الموضوع كيفيه تمكين تكامل Microsoft Dynamics 365 Commerce وMicrosoft Teams.
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
ms.openlocfilehash: c0dbf7a3c7fa3532e35cac240c1abb8adbdbe489
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 04/01/2021
ms.locfileid: "5842605"
---
# <a name="enable-dynamics-365-commerce-and-microsoft-teams-integration"></a><span data-ttu-id="acea8-103">تمكين تكامل Dynamics 365 Commerce وMicrosoft Teams</span><span class="sxs-lookup"><span data-stu-id="acea8-103">Enable Dynamics 365 Commerce and Microsoft Teams integration</span></span>

[!include [banner](includes/banner.md)]
[!include [banner](includes/preview-banner.md)]

<span data-ttu-id="acea8-104">يوضح هذا الموضوع كيفيه تمكين تكامل Microsoft Dynamics 365 Commerce وMicrosoft Teams.</span><span class="sxs-lookup"><span data-stu-id="acea8-104">This topic describes how to enable Microsoft Dynamics 365 Commerce and Microsoft Teams integration.</span></span>

<span data-ttu-id="acea8-105">لتوفير Teams مع المعلومات من Dynamics 365 Commerce ومزامنة ميزات أداره المهام بين فرق العمل وتطبيق نقطه البيع (POS)، يجب تمكين ميزات التكامل في إدارة Commerce.</span><span class="sxs-lookup"><span data-stu-id="acea8-105">To provision Teams with information from Dynamics 365 Commerce and synchronize the task management features between Teams and the point of sale (POS) application, you must enable the integration features in Commerce headquarters.</span></span>

> [!NOTE]
> <span data-ttu-id="acea8-106">عند تمكين تكامل Teams، فأنت توافق علي مشاركه البيانات مع فرق العمل.</span><span class="sxs-lookup"><span data-stu-id="acea8-106">When you enable Teams integration, you consent to share your data with Teams.</span></span> <span data-ttu-id="acea8-107">وقد تتواجد البيانات المشتركة مع Teams في بلد مختلف عن بيانات Commerce الخاصة بك، وقد يكون عرضه لمعايير توافق مختلفه.</span><span class="sxs-lookup"><span data-stu-id="acea8-107">Data that is shared with Teams might reside in a different country than your Commerce data, and it might be subject to different compliance standards.</span></span> <span data-ttu-id="acea8-108">لمزيد من المعلومات، راجع [Microsoft Trust Center](https://www.microsoft.com/trust-center).</span><span class="sxs-lookup"><span data-stu-id="acea8-108">For more information, see the [Microsoft Trust Center](https://www.microsoft.com/trust-center).</span></span> <span data-ttu-id="acea8-109">للحصول علي معلومات حول سياسات خصوصية Microsoft، راجع [بيان خصوصية Microsoft ](https://aka.ms/privacy).</span><span class="sxs-lookup"><span data-stu-id="acea8-109">For information about Microsoft privacy policies, see the [Microsoft Privacy Statement](https://aka.ms/privacy).</span></span>

## <a name="enable-teams-integration"></a><span data-ttu-id="acea8-110">تمكين تكامل Teams</span><span class="sxs-lookup"><span data-stu-id="acea8-110">Enable Teams integration</span></span>

<span data-ttu-id="acea8-111">قبل ان تتمكن من تمكين تكامل Microsoft Teams مع Commerce، يجب تسجيل تطبيق Teams مع المستاجر الخاص بك في مدخل Azure.</span><span class="sxs-lookup"><span data-stu-id="acea8-111">Before you can enable Microsoft Teams integration with Commerce, you must register the Teams application with your tenant in the Azure portal.</span></span>

<span data-ttu-id="acea8-112">لتسجيل تطبيق Teams مع المستاجر الخاص بك في مدخل Azure، اتبع الخطوات التالية.</span><span class="sxs-lookup"><span data-stu-id="acea8-112">To register the Teams application with your tenant in the Azure portal, follow these steps.</span></span>

1. <span data-ttu-id="acea8-113">اتبع الخطوات الموجودة في [بدء التشغيل السريع: تسجيل تطبيق في النظام الأساسي لهوية Microsoft](https://docs.microsoft.com/azure/active-directory/develop/quickstart-register-app) لتسجيل تطبيق Teams مع المستأجر الخاص بك في مدخل Azure.</span><span class="sxs-lookup"><span data-stu-id="acea8-113">Follow the steps in [Quickstart: Register an app in the Microsoft identity platform](https://docs.microsoft.com/azure/active-directory/develop/quickstart-register-app) to register the Teams application with your tenant in the Azure portal.</span></span>
1. <span data-ttu-id="acea8-114">انسخ قيمة **معرف التطبيق (العميل)** من صفحة **النظرة العامة** للتطبيق المسجل.</span><span class="sxs-lookup"><span data-stu-id="acea8-114">Copy the **Application (client) ID** value from the **Overview** page for the registered app.</span></span> <span data-ttu-id="acea8-115">ستستخدم هذه القيمة لتمكين تكامل Teams في إدارة Commerce.</span><span class="sxs-lookup"><span data-stu-id="acea8-115">You will use this value to enable Teams integration in Commerce headquarters.</span></span>
1. <span data-ttu-id="acea8-116">انسخ قيمه الشهادة التي تم إدخالها عند [إضافة شهادة](https://docs.microsoft.com/azure/active-directory/develop/quickstart-register-app#add-a-certificate) في الخطوة 1.</span><span class="sxs-lookup"><span data-stu-id="acea8-116">Copy the certificate value that was entered when you [added a certificate](https://docs.microsoft.com/azure/active-directory/develop/quickstart-register-app#add-a-certificate) in step 1.</span></span> <span data-ttu-id="acea8-117">تُعرف الشهادة أيضا باسم المفتاح العام أو مفتاح التطبيق.</span><span class="sxs-lookup"><span data-stu-id="acea8-117">The certificate is also known as the public key or application key.</span></span> <span data-ttu-id="acea8-118">ستستخدم هذه القيمة لتمكين تكامل Teams في إدارة Commerce.</span><span class="sxs-lookup"><span data-stu-id="acea8-118">You will use this value to enable Teams integration in Commerce headquarters.</span></span>

<span data-ttu-id="acea8-119">لتمكين تكامل Teams في إدارة Commerce، اتبع هذه الخطوات.</span><span class="sxs-lookup"><span data-stu-id="acea8-119">To enable Teams integration in Commerce headquarters, follow these steps.</span></span>

1. <span data-ttu-id="acea8-120">انتقل إلى **Retail وCommerce \> إعداد القناة \> تكوين تكامل Microsoft Teams**.</span><span class="sxs-lookup"><span data-stu-id="acea8-120">Go to **Retail and Commerce \> Channel setup \> Microsoft Teams integration configuration**.</span></span>
1. <span data-ttu-id="acea8-121">في جزء الإجراءات، حدد **تحرير**.</span><span class="sxs-lookup"><span data-stu-id="acea8-121">On the Action Pane, select **Edit**.</span></span>
1. <span data-ttu-id="acea8-122">قم بتعيين خيار **تمكين تكامل Microsoft Teams** إلى **نعم**.</span><span class="sxs-lookup"><span data-stu-id="acea8-122">Set the **Enable Microsoft Teams integration** option to **Yes**.</span></span>
1. <span data-ttu-id="acea8-123">في حقلي **معرف التطبيق** و **مفتاح التطبيق**، أدخل القيم التي حصلت عليها عندما قمت بتسجيل تطبيق Teams في مدخل Azure.</span><span class="sxs-lookup"><span data-stu-id="acea8-123">In the **Application ID** and **Application key** fields, enter the values you obtained when you registered the Teams application in the Azure portal.</span></span>
1. <span data-ttu-id="acea8-124">في جزء الإجراءات، حدد **حفظ**.</span><span class="sxs-lookup"><span data-stu-id="acea8-124">On the Action Pane, select **Save**.</span></span>

<span data-ttu-id="acea8-125">يبين الرسم التوضيحي التالي مثالا لتكوين تكامل Teams في إدارة Commerce.</span><span class="sxs-lookup"><span data-stu-id="acea8-125">The following illustration shows an example of the configuration of Teams integration in Commerce headquarters.</span></span>

![تكوين تكامل Teams في إداره Commerce](media/D365-Commerce-Microsoft-Teams-Configuration_with_disclaimer.png)

## <a name="disable-teams-integration"></a><span data-ttu-id="acea8-127">تعطيل تكامل Teams</span><span class="sxs-lookup"><span data-stu-id="acea8-127">Disable Teams integration</span></span>

<span data-ttu-id="acea8-128">لتعطيل تكامل Microsoft Teams في إدارة Commerce، اتبع هذه الخطوات.</span><span class="sxs-lookup"><span data-stu-id="acea8-128">To disable Microsoft Teams integration in Commerce headquarters, follow these steps.</span></span>

1. <span data-ttu-id="acea8-129">انتقل إلى **Retail وCommerce \> إعداد القناة \> Microsoft Teams تكوين التكامل**.</span><span class="sxs-lookup"><span data-stu-id="acea8-129">Go to **Retail and Commerce \> Channel setup \> Microsoft Teams Integration Configuration**.</span></span>
1. <span data-ttu-id="acea8-130">في جزء الإجراءات، حدد **تحرير**.</span><span class="sxs-lookup"><span data-stu-id="acea8-130">On the Action Pane, select **Edit**.</span></span>
3. <span data-ttu-id="acea8-131">قم بتعيين خيار **تمكين تكامل Microsoft Teams** إلى **لا**.</span><span class="sxs-lookup"><span data-stu-id="acea8-131">Set the **Enable Microsoft Teams integration** option to **No**.</span></span>
4. <span data-ttu-id="acea8-132">امسح القيم من حقلي **معرف التطبيق** و **مفتاح التطبيق**.</span><span class="sxs-lookup"><span data-stu-id="acea8-132">Clear the values from the **Application ID** and **Application Key** fields.</span></span>
1. <span data-ttu-id="acea8-133">في جزء الإجراءات، حدد **حفظ**.</span><span class="sxs-lookup"><span data-stu-id="acea8-133">On the Action Pane, select **Save**.</span></span>

> [!NOTE]
> <span data-ttu-id="acea8-134">بعد قيامك بتعطيل تكامل Teams مع Commerce، لن تعرض أجهزة نقطة البيع الطرفية المهام التي تم ترحيلها من تطبيق Teams.</span><span class="sxs-lookup"><span data-stu-id="acea8-134">After you disable Teams integration with Commerce, POS terminals will no longer show tasks that are published from the Teams application.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="acea8-135">الموارد الإضافية</span><span class="sxs-lookup"><span data-stu-id="acea8-135">Additional resources</span></span>

[<span data-ttu-id="acea8-136">نظرة عامة على تكامل Dynamics 365 Commerce وMicrosoft Teams</span><span class="sxs-lookup"><span data-stu-id="acea8-136">Dynamics 365 Commerce and Microsoft Teams integration overview</span></span>](commerce-teams-integration.md)

[<span data-ttu-id="acea8-137">توفير Microsoft Teams من Dynamics 365 Commerce</span><span class="sxs-lookup"><span data-stu-id="acea8-137">Provision Microsoft Teams from Dynamics 365 Commerce</span></span>](provision-teams-from-commerce.md)

[<span data-ttu-id="acea8-138">مزامنة إدارة المهام بين Microsoft Teams ونقطة بيع Dynamics 365 Commerce</span><span class="sxs-lookup"><span data-stu-id="acea8-138">Synchronize task management between Microsoft Teams and Dynamics 365 Commerce POS</span></span>](synchronize-tasks-teams-pos.md)

[<span data-ttu-id="acea8-139">إدارة أدوار المستخدمين في Microsoft Teams</span><span class="sxs-lookup"><span data-stu-id="acea8-139">Manage user roles in Microsoft Teams</span></span>](manage-user-roles-teams.md)

[<span data-ttu-id="acea8-140">تعيين المتاجر والفرق عند وجود فرق موجودة مسبقًا في Microsoft Teams</span><span class="sxs-lookup"><span data-stu-id="acea8-140">Map stores and teams if there are pre-existing teams in Microsoft Teams</span></span>](map-stores-existing-teams.md)

[<span data-ttu-id="acea8-141">الأسئلة الشائعة حول تكامل Dynamics 365 Commerce وMicrosoft Teams</span><span class="sxs-lookup"><span data-stu-id="acea8-141">Dynamics 365 Commerce and Microsoft Teams integration FAQ</span></span>](teams-integration-faq.md)
