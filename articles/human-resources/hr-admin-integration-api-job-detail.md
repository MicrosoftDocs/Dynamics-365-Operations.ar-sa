---
title: واجهة API لتفاصيل الوظيفة
description: يوفر هذا الموضوع تفاصيل ومثال استعلام لكيان تفاصيل الوظيفة في Dynamics 365 Human Resources.
author: jcart
manager: tfehr
ms.date: 04/07/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: anbichse
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: jcart
ms.search.validFrom: 2021-04-07
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 4f15282bf72340cb1a832ff3264361472d0a6c70
ms.sourcegitcommit: d18d9cdb175c9d42eafbed66352c24b2aa94258b
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 04/13/2021
ms.locfileid: "5881917"
---
# <a name="job-detail-api"></a><span data-ttu-id="25fc3-103">واجهة API لتفاصيل الوظيفة</span><span class="sxs-lookup"><span data-stu-id="25fc3-103">Job detail API</span></span>

<span data-ttu-id="25fc3-104">يوفر هذا الموضوع تفاصيل ومثال استعلام لكيان تفاصيل الوظيفة في Dynamics 365 Human Resources.</span><span class="sxs-lookup"><span data-stu-id="25fc3-104">This topic provides details and an example query for the Job detail entity in Dynamics 365 Human Resources.</span></span>

## <a name="properties"></a><span data-ttu-id="25fc3-105">الخصائص</span><span class="sxs-lookup"><span data-stu-id="25fc3-105">Properties</span></span>

| <span data-ttu-id="25fc3-106">الخاصية</span><span class="sxs-lookup"><span data-stu-id="25fc3-106">Property</span></span><br><span data-ttu-id="25fc3-107">**الاسم الفعلي**</span><span class="sxs-lookup"><span data-stu-id="25fc3-107">**Physical name**</span></span><br><span data-ttu-id="25fc3-108">**_النوع_**</span><span class="sxs-lookup"><span data-stu-id="25fc3-108">**_Type_**</span></span> | <span data-ttu-id="25fc3-109">استخدام</span><span class="sxs-lookup"><span data-stu-id="25fc3-109">Use</span></span> | <span data-ttu-id="25fc3-110">الوصف</span><span class="sxs-lookup"><span data-stu-id="25fc3-110">Description</span></span> |
| --- | --- | --- |
| <span data-ttu-id="25fc3-111">**معرف الوظيفة**</span><span class="sxs-lookup"><span data-stu-id="25fc3-111">**Job ID**</span></span><br><span data-ttu-id="25fc3-112">mshr_jobid</span><span class="sxs-lookup"><span data-stu-id="25fc3-112">mshr_jobid</span></span><br><span data-ttu-id="25fc3-113">*سلسلة*</span><span class="sxs-lookup"><span data-stu-id="25fc3-113">*String*</span></span> | <span data-ttu-id="25fc3-114">للقراءة فقط</span><span class="sxs-lookup"><span data-stu-id="25fc3-114">Read-only</span></span><br><span data-ttu-id="25fc3-115">مطلوب</span><span class="sxs-lookup"><span data-stu-id="25fc3-115">Required</span></span> | <span data-ttu-id="25fc3-116">معرف فريد لوظيفة.</span><span class="sxs-lookup"><span data-stu-id="25fc3-116">Unique ID for a job.</span></span> |
| <span data-ttu-id="25fc3-117">**الحد الأدنى لسعر السوق**</span><span class="sxs-lookup"><span data-stu-id="25fc3-117">**Market price low threshold**</span></span><br><span data-ttu-id="25fc3-118">mshr_marketpricelowthreshold</span><span class="sxs-lookup"><span data-stu-id="25fc3-118">mshr_marketpricelowthreshold</span></span><br><span data-ttu-id="25fc3-119">*عشري*</span><span class="sxs-lookup"><span data-stu-id="25fc3-119">*Decimal*</span></span> | | <span data-ttu-id="25fc3-120">قيمة معرف GUID منشأ بواسطة النظام لتعريف المنصب بشكل فريد.</span><span class="sxs-lookup"><span data-stu-id="25fc3-120">A system-generated GUID value to uniquely identify the position.</span></span>  |
