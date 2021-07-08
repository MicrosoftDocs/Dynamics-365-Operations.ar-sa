---
title: Regulatory Configuration Service (RCS) - حذف بيئة RCS
description: يشرح هذا الموضوع كيف يمكن لمسؤول نظام Regulatory Configuration Service (RCS) حذف بيئة RCS والبيانات ذات الصلة.
author: JaneA07
ms.date: 06/14/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: RCS, Regulatory Configuration Services, Localization, Global
audience: Application User, System Admin
ms.reviewer: kfend
ms.custom: 97423
ms.assetid: ''
ms.search.region: Global
ms.author: janeaug
ms.search.validFrom: 2021-01-01
ms.dyn365.ops.version: AX 10.0.15
ms.openlocfilehash: 637962cf63bfd8c2330726f33545f939ec91d58d
ms.sourcegitcommit: dbffde1944b9d037124415c28053036c9ef1ecb7
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 06/23/2021
ms.locfileid: "6295808"
---
# <a name="regulatory-configuration-service-rcs---delete-an-rcs-environment"></a><span data-ttu-id="78f45-103">Regulatory Configuration Service (RCS) - حذف بيئة RCS</span><span class="sxs-lookup"><span data-stu-id="78f45-103">Regulatory Configuration Service (RCS) - Delete an RCS environment</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="78f45-104">يشرح هذا الموضوع كيف يمكن لمسؤول نظام Regulatory Configuration Service (RCS) حذف بيئة RCS والبيانات ذات الصلة.</span><span class="sxs-lookup"><span data-stu-id="78f45-104">This topic explains how a Regulatory Configuration Service (RCS) system administrator can delete an RCS environment and related data.</span></span>

<span data-ttu-id="78f45-105">قبل أن تتمكن من استكمال الإجراء في هذا الموضوع، يجب تلبية المتطلبات التالية:</span><span class="sxs-lookup"><span data-stu-id="78f45-105">Before you can complete the procedure in this topic, the following prerequisites must be met:</span></span>

- <span data-ttu-id="78f45-106">يجب تعيين دور **مسؤول النظام** لك لبيئة RCS.</span><span class="sxs-lookup"><span data-stu-id="78f45-106">You must have the **System Admin** role assigned to you for the RCS environment.</span></span>
- <span data-ttu-id="78f45-107">يجب أن يحتوي دور **مسؤول النظام** على دور **RCSDeleteEnvironmentDuty** معين إليه.</span><span class="sxs-lookup"><span data-stu-id="78f45-107">The **System Admin** role must have the **RCSDeleteEnvironmentDuty** role assigned to it.</span></span>

## <a name="delete-an-rcs-environment"></a><span data-ttu-id="78f45-108">حذف بيئة RCS</span><span class="sxs-lookup"><span data-stu-id="78f45-108">Delete an RCS environment</span></span>

1. <span data-ttu-id="78f45-109">افتح RCS، وحدد لوحة مساحة عمل **التقارير الإلكترونية**.</span><span class="sxs-lookup"><span data-stu-id="78f45-109">Open RCS, and select the **Electronic reporting** workspace tile.</span></span>
2. <span data-ttu-id="78f45-110">في القسم **ارتباطات ذات صلة**، حدد **حذف بيئة RCS**.</span><span class="sxs-lookup"><span data-stu-id="78f45-110">In the **Related links** section, select **Delete RCS environment**.</span></span>

    ![حذف ارتباط بيئة RCS في قسم ارتباطات ذات صلة](media/01_RCS-Delete-Environ-Related-Link.PNG)

3. <span data-ttu-id="78f45-112">في مربع الحوار الذي يظهر، راجع الرسائل حول نطاق حذف البيئة.</span><span class="sxs-lookup"><span data-stu-id="78f45-112">In the dialog box that appears, review the messages about the scope of environment deletion.</span></span>

    ![الرسائل الموجودة في مربع الحوار حذف بيئة RCS](media/01_RCS-Delete-Environ-Msg_noGUID.PNG)

    > [!IMPORTANT]
    > <span data-ttu-id="78f45-114">لا يمكن عكس حذف بيئة RCS.</span><span class="sxs-lookup"><span data-stu-id="78f45-114">Deletion of an RCS environment can't be reversed.</span></span>
    >
    > <span data-ttu-id="78f45-115">تقوم العملية بحذف بيئة RCS المحددة وأية بيانات مرتبطة، بما في ذلك الميزات والتكوينات المخزنة في المستودع العالمي.</span><span class="sxs-lookup"><span data-stu-id="78f45-115">The operation deletes the selected RCS environment and any related data, including features and configurations that are stored in the Global repository.</span></span> <span data-ttu-id="78f45-116">لن يتم إلغاء مشاركة الميزات والتكوينات المشتركة مع المؤسسات الأخرى ويتم حذفها إذا لم يكن لديها تبعيات.</span><span class="sxs-lookup"><span data-stu-id="78f45-116">Features and configurations that are shared with other organizations will be unshared and deleted if they have no dependencies.</span></span> <span data-ttu-id="78f45-117">سيتم وضع علامة موقوف على الميزات والتكوينات التي لها تبعيات.</span><span class="sxs-lookup"><span data-stu-id="78f45-117">Features and configurations that have dependencies will be marked as discontinued.</span></span>

4. <span data-ttu-id="78f45-118">في الحقل الذي يتم توفيره، أدخل المعرّف الفريد العمومي (GUID) الخاص ببيئة RCS لتأكيد رغبتك في حذفه.</span><span class="sxs-lookup"><span data-stu-id="78f45-118">In the field that is provided, enter the globally unique identifier (GUID) of the RCS environment to confirm that you want to delete it.</span></span> <span data-ttu-id="78f45-119">يتم تضمين المعرّف الفريد العمومي (GUID) الخاص بالبيئة في رسالة الحذف.</span><span class="sxs-lookup"><span data-stu-id="78f45-119">The environment's GUID is included in the deletion message.</span></span>
5. <span data-ttu-id="78f45-120">حدد **حذف البيئة**.</span><span class="sxs-lookup"><span data-stu-id="78f45-120">Select **Delete environment**.</span></span>
    
<span data-ttu-id="78f45-121">يتم الآن حذف بيئة RCS الخاصة بك وأية بيانات مرتبطة.</span><span class="sxs-lookup"><span data-stu-id="78f45-121">Your RCS environment and any related data are now deleted.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="78f45-122">بعد حذف بيئة RCS، لا توجد طريقة لاسترداد البيانات.</span><span class="sxs-lookup"><span data-stu-id="78f45-122">After you delete an RCS environment, there is no way to recover the data.</span></span> <span data-ttu-id="78f45-123">يمكن إنشاء بيئة RCS جديدة في أي منطقة RCS متوفرة.</span><span class="sxs-lookup"><span data-stu-id="78f45-123">A new RCS environment can be created in any available RCS region.</span></span>
