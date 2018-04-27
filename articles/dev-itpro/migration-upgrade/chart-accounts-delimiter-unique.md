---
title: "يجب أن يكون محدد دليل الحسابات فريدًا"
description: "في Dynamics 365 for Finance and Operations، لا يمكنك الحصول على نفس المحدد لدليل الحسابات وقيم الأبعاد. يجب عليك تغيير قيم المحددات بعد الترقية."
author: ryansandness
manager: AnnBe
ms.date: 03/30/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.custom: 265364
ms.assetid: c61391e4-c4bf-4f09-bd18-8107a1bf055e
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: 8
ms.translationtype: HT
ms.sourcegitcommit: a8b5a5af5108744406a3d2fb84d7151baea2481b
ms.openlocfilehash: c9728714944b54f3bff1e2a8b43c7adcf5200f08
ms.contentlocale: ar-sa
ms.lasthandoff: 04/13/2018

---

# <a name="chart-of-accounts-delimiter-must-be-unique"></a><span data-ttu-id="59532-104">يجب أن يكون محدد دليل الحسابات فريدًا</span><span class="sxs-lookup"><span data-stu-id="59532-104">Chart of accounts delimiter must be unique</span></span>

[!INCLUDE [banner](../includes/banner.md)]

<span data-ttu-id="59532-105">في Microsoft Dynamics AX 2012، يمكنك استخدام نفس المحدد لدليل الحسابات وقيم الأبعاد.</span><span class="sxs-lookup"><span data-stu-id="59532-105">In Microsoft Dynamics AX 2012, you could use the same delimiter for your chart of accounts and dimension values.</span></span> <span data-ttu-id="59532-106">في Dynamics 365 for Finance and Operations، لا يمكنك الحصول على نفس المحدد لدليل الحسابات وقيم الأبعاد.</span><span class="sxs-lookup"><span data-stu-id="59532-106">In Dynamics 365 for Finance and Operations, you cannot have the same delimiter for the chart of accounts and dimension values.</span></span> <span data-ttu-id="59532-107">في حالة وجود محدد مكرر، يمكنك تغييره بعد الترقية.</span><span class="sxs-lookup"><span data-stu-id="59532-107">If there is a duplicate delimiter, you can change it after upgrade.</span></span> 

<span data-ttu-id="59532-108">تتوفر هذه الميزة في:</span><span class="sxs-lookup"><span data-stu-id="59532-108">This feature is available in:</span></span>
- <span data-ttu-id="59532-109">Dynamics 365 for Finance and Operations، الإصدار 8.0</span><span class="sxs-lookup"><span data-stu-id="59532-109">Dynamics 365 for Finance and Operations version 8.0</span></span>
- <span data-ttu-id="59532-110">في Dynamics 365 for Finance and Operations الإصدار 7.1، لا يمكن لقاعدة المعارف KB 4094701 إدخال الأبعاد المالية عندما تحتوي قيم الأبعاد على محدد دليل الحسابات</span><span class="sxs-lookup"><span data-stu-id="59532-110">Dynamics 365 for Finance and Operations version 7.1, KB 4094701 Cannot enter the financial dimensions when the dimension values contain the chart of accounts delimiter</span></span>
- <span data-ttu-id="59532-111">في Dynamics 365 for Finance and Operations الإصدار 7.2، لا يمكن لقاعدة المعارف 4092967 اختيار مشروع فرعي مثل بُعد عندما يحتوي تنسيق مشروع فرعي على محدد أبعاد</span><span class="sxs-lookup"><span data-stu-id="59532-111">Dynamics 365 for Finance and Operations version 7.2, KB 4092967 Cannot choose sub-project as dimension when sub-project format contains the dimension delimiter</span></span>

## <a name="update-delimiter"></a><span data-ttu-id="59532-112">تحديث المحدد</span><span class="sxs-lookup"><span data-stu-id="59532-112">Update delimiter</span></span>
<span data-ttu-id="59532-113">في حالة وجود تعارض في "دليل الحسابات"، يمكن تغيير محدد دليل الحسابات وتنسيق معرف المشروع/المشروع الفرعي.</span><span class="sxs-lookup"><span data-stu-id="59532-113">If there is a conflict with the Chart of Accounts, the Chart of accounts delimiter and the project/subproject ID format can be changed.</span></span> <span data-ttu-id="59532-114">لا يمكن تغيير أي محددات أبعاد أخرى.</span><span class="sxs-lookup"><span data-stu-id="59532-114">No other dimension delimiters can be changed.</span></span> 
- <span data-ttu-id="59532-115">يمكنك تغيير محدد دليل الحسابات بعد الترقية إلى Finance and Operations في **محددات دفتر الأستاذ العام** > **دليل الحسابات والأبعاد** > **تغيير محدد**.</span><span class="sxs-lookup"><span data-stu-id="59532-115">You can change the chart of accounts delimiter after upgrade to Finance and Operations in **General ledger parameters** > **Chart of accounts and dimensions** > **Change delimiter**.</span></span> 
- <span data-ttu-id="59532-116">إذا كان التعارض فقط في تنسيق معرف المشروع/المشروع الفرعي، يمكنك تغيير هذه القيمة في **محددات المحاسبة وإدارة المشروع** > **عام** > **تعديل تنسيق المشروع الفرعي**.</span><span class="sxs-lookup"><span data-stu-id="59532-116">If the only conflict is with the project/subproject ID format, you can change that value in **Project management and accounting parameters** > **General** > **Modify subproject format**.</span></span> 

## <a name="how-to-determine-if-your-environment-requires-updated-delimiters"></a><span data-ttu-id="59532-117">كيفية تحديد ما إذا كانت البيئة الخاصة بك تتطلب محددات محدَّثة</span><span class="sxs-lookup"><span data-stu-id="59532-117">How to determine if your environment requires updated delimiters</span></span> 
<span data-ttu-id="59532-118">في حالة حدوث تعارض بين المحددات الموجودة في البيئة الخاصة بك التي تمت ترقيتها، تواجه عدم استقرار عند إدخال قيم في عنصر تحكم الإدخال المقسَّم أو عنصر تحكم إدخال الأبعاد.</span><span class="sxs-lookup"><span data-stu-id="59532-118">If delimiters in your upgraded environment are conflicting, you may experience instability when entering values in a segmented entry control or dimension entry control.</span></span> <span data-ttu-id="59532-119">ويعني هذا أنك ستحتاج دائمًا إلى استخدام عمليات بحث أو قائمة منبثقة عند إدخال مجموعات الحسابات والأبعاد.</span><span class="sxs-lookup"><span data-stu-id="59532-119">This means that you will need to always use lookups or a flyout menu when entering account and dimension combinations.</span></span>

