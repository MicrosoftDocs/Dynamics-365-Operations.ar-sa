---
title: استكشاف المشاكل ذات الصلة بإدراك الحلول وإصلاحها
description: يوفر هذا الموضوع استكشاف الأخطاء وإصلاحها الذي يمكن أن يساعدك في إصلاح المشكلات ذات الصلة بإدراك الحلول.
author: RamaKrishnamoorthy
manager: AnnBe
ms.date: 03/16/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-03-16
ms.openlocfilehash: 013e37269ec3df2bede15b28cffcc175967de9a3
ms.sourcegitcommit: 68f1485de7d64a6c9eba1088af63bd07992d972d
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 03/27/2020
ms.locfileid: "3172611"
---
# <a name="troubleshoot-issues-related-to-solution-awareness"></a><span data-ttu-id="a292d-103">استكشاف المشاكل ذات الصلة بإدراك الحلول وإصلاحها</span><span class="sxs-lookup"><span data-stu-id="a292d-103">Troubleshoot issues related to solution awareness</span></span>

[!include [banner](../../includes/banner.md)]



<span data-ttu-id="a292d-104">يوفر هذا الموضوع معلومات حول استكشاف أخطاء تكامل الكتابة الثنائية وإصلاحها بين تطبيقات Finance and Operations وCommon Data Service.</span><span class="sxs-lookup"><span data-stu-id="a292d-104">This topic provides troubleshooting information for dual-write integration between Finance and Operations apps and Common Data Service.</span></span> <span data-ttu-id="a292d-105">على وجه التحديد، يوفر هذا الموضوع المعلومات التي يمكن أن تساعدك في إصلاح المشكلات ذات الصلة بإدراك الحلول.</span><span class="sxs-lookup"><span data-stu-id="a292d-105">Specifically, it provides information that can help you fix issues that are related to solution awareness.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="a292d-106">قد تتطلب بعض المشكلات التي يتناولها هذا الموضوع إما دور إدارة النظام أو بيانات اعتماد مسؤول مستأجر  Microsoft Azure Active Directory (Azure AD).</span><span class="sxs-lookup"><span data-stu-id="a292d-106">Some of the issues that this topic addresses might require either the system admin role or Microsoft Azure Active Directory (Azure AD) tenant admin credentials.</span></span> <span data-ttu-id="a292d-107">يوضح القسم الخاص بكل مشكلة ما إذا كانت هناك حاجة إلى دور محدد أو بيانات اعتماد.</span><span class="sxs-lookup"><span data-stu-id="a292d-107">The section for each issue explains whether a specific role or credentials are required.</span></span>

## <a name="error-on-the-dual-write-page"></a><span data-ttu-id="a292d-108">خطأ في صفحة الكتابة الثنائية</span><span class="sxs-lookup"><span data-stu-id="a292d-108">Error on the Dual-write page</span></span>

<span data-ttu-id="a292d-109">في صفحة **الكتابة الثنائية**، قد تتلقي رسالة خطأ مشابهة للمثال التالي:</span><span class="sxs-lookup"><span data-stu-id="a292d-109">On the **Dual-write** page, you might receive an error message that resembles the following example:</span></span>

<span data-ttu-id="a292d-110">*لم يتم العثور على الكيان باسم 'msdyn\_dualwriteentitymap' with namemapping='Logical' في MetadataCache.*</span><span class="sxs-lookup"><span data-stu-id="a292d-110">*The entity with a name 'msdyn\_dualwriteentitymap' with namemapping='Logical' was not found in the MetadataCache.*</span></span>

<span data-ttu-id="a292d-111">لإصلاح المشكلة، تأكد من تثبيت الحل الأساسي للكتابة الثنائية في Common Data Service.</span><span class="sxs-lookup"><span data-stu-id="a292d-111">To fix the issue, make sure that the dual-write core solution is installed in Common Data Service.</span></span> <span data-ttu-id="a292d-112">يُعد الحل الأساسي للكتابة الثنائية متطلبًا أساسيًا لمعرفة الحلول.</span><span class="sxs-lookup"><span data-stu-id="a292d-112">The dual-write core solution is a prerequisite for solution awareness.</span></span>