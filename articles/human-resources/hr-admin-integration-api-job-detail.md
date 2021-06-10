---
title: واجهة API لتفاصيل الوظيفة
description: يوفر هذا الموضوع تفاصيل ومثال استعلام لكيان تفاصيل الوظيفة في Dynamics 365 Human Resources.
author: jcart
ms.date: 04/07/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: jcart
ms.search.validFrom: 2021-04-07
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 562b9f505311b6cfe505a76fc5c0a384eb641936
ms.sourcegitcommit: 879ee8a10e6158885795dce4b3db5077540eec41
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 05/18/2021
ms.locfileid: "6054754"
---
# <a name="job-detail-api"></a><span data-ttu-id="09b79-103">واجهة API لتفاصيل الوظيفة</span><span class="sxs-lookup"><span data-stu-id="09b79-103">Job detail API</span></span>

<span data-ttu-id="09b79-104">يوفر هذا الموضوع تفاصيل ومثال استعلام لكيان تفاصيل الوظيفة في Dynamics 365 Human Resources.</span><span class="sxs-lookup"><span data-stu-id="09b79-104">This topic provides details and an example query for the Job detail entity in Dynamics 365 Human Resources.</span></span>

## <a name="properties"></a><span data-ttu-id="09b79-105">الخصائص</span><span class="sxs-lookup"><span data-stu-id="09b79-105">Properties</span></span>

| <span data-ttu-id="09b79-106">الخاصية</span><span class="sxs-lookup"><span data-stu-id="09b79-106">Property</span></span><br><span data-ttu-id="09b79-107">**الاسم الفعلي**</span><span class="sxs-lookup"><span data-stu-id="09b79-107">**Physical name**</span></span><br><span data-ttu-id="09b79-108">**_النوع_**</span><span class="sxs-lookup"><span data-stu-id="09b79-108">**_Type_**</span></span> | <span data-ttu-id="09b79-109">استخدام</span><span class="sxs-lookup"><span data-stu-id="09b79-109">Use</span></span> | <span data-ttu-id="09b79-110">الوصف</span><span class="sxs-lookup"><span data-stu-id="09b79-110">Description</span></span> |
| --- | --- | --- |
| <span data-ttu-id="09b79-111">**معرف الوظيفة**</span><span class="sxs-lookup"><span data-stu-id="09b79-111">**Job ID**</span></span><br><span data-ttu-id="09b79-112">mshr_jobid</span><span class="sxs-lookup"><span data-stu-id="09b79-112">mshr_jobid</span></span><br><span data-ttu-id="09b79-113">*سلسلة*</span><span class="sxs-lookup"><span data-stu-id="09b79-113">*String*</span></span> | <span data-ttu-id="09b79-114">للقراءة فقط</span><span class="sxs-lookup"><span data-stu-id="09b79-114">Read-only</span></span><br><span data-ttu-id="09b79-115">مطلوب</span><span class="sxs-lookup"><span data-stu-id="09b79-115">Required</span></span> | <span data-ttu-id="09b79-116">معرف فريد لوظيفة.</span><span class="sxs-lookup"><span data-stu-id="09b79-116">Unique ID for a job.</span></span> |
| <span data-ttu-id="09b79-117">**الحد الأدنى لسعر السوق**</span><span class="sxs-lookup"><span data-stu-id="09b79-117">**Market price low threshold**</span></span><br><span data-ttu-id="09b79-118">mshr_marketpricelowthreshold</span><span class="sxs-lookup"><span data-stu-id="09b79-118">mshr_marketpricelowthreshold</span></span><br><span data-ttu-id="09b79-119">*عشري*</span><span class="sxs-lookup"><span data-stu-id="09b79-119">*Decimal*</span></span> | | <span data-ttu-id="09b79-120">قيمة معرف GUID منشأ بواسطة النظام لتعريف المنصب بشكل فريد.</span><span class="sxs-lookup"><span data-stu-id="09b79-120">A system-generated GUID value to uniquely identify the position.</span></span>  |
