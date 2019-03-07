---
title: جعل محدد دليل الحسابات فريدًا
description: في Dynamics 365 for Finance and Operations، لا يمكن أن يكون محدد دليل الحسابات هو نفسه محدد قيم الأبعاد. يجب عليك تغيير قيم المحددات بعد الترقية.
author: ryansandness
manager: AnnBe
ms.date: 03/30/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: 265364
ms.assetid: c61391e4-c4bf-4f09-bd18-8107a1bf055e
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: 8
ms.openlocfilehash: e197a1b44e038a97b8bf6db692dcc2eef2bc5f7b
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 01/29/2019
ms.locfileid: "335843"
---
# <a name="make-the-chart-of-accounts-delimiter-unique"></a><span data-ttu-id="e0ec0-104">جعل محدد دليل الحسابات فريدًا</span><span class="sxs-lookup"><span data-stu-id="e0ec0-104">Make the chart of accounts delimiter unique</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="e0ec0-105">في Microsoft Dynamics AX 2012، يمكنك استخدام المحدد نفسه لدليل الحسابات وقيم الأبعاد.</span><span class="sxs-lookup"><span data-stu-id="e0ec0-105">In Microsoft Dynamics AX 2012, you could use the same delimiter for your chart of accounts and dimension values.</span></span> <span data-ttu-id="e0ec0-106">في Dynamics 365 for Finance and Operations، لا يمكن أن يكون محدد دليل الحسابات هو نفسه محدد قيم الأبعاد.</span><span class="sxs-lookup"><span data-stu-id="e0ec0-106">In Dynamics 365 for Finance and Operations, you cannot have the same delimiter for the chart of accounts and dimension values.</span></span> <span data-ttu-id="e0ec0-107">في حالة وجود محدد مكرر، يمكنك تغييره بعد الترقية.</span><span class="sxs-lookup"><span data-stu-id="e0ec0-107">If there is a duplicate delimiter, you can change it after upgrade.</span></span> 

<span data-ttu-id="e0ec0-108">تتوفر هذه الميزة في:</span><span class="sxs-lookup"><span data-stu-id="e0ec0-108">This feature is available in:</span></span>
- <span data-ttu-id="e0ec0-109">الإصدار 8.0 من Dynamics 365 for Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="e0ec0-109">Dynamics 365 for Finance and Operations version 8.0</span></span>
- <span data-ttu-id="e0ec0-110">Dynamics 365 for Finance and Operations، الإصدار 7.1، KB 4094701 لا يمكن إدخال الأبعاد المالية عندما تحتوي قيم الأبعاد على محدد دليل الحسابات</span><span class="sxs-lookup"><span data-stu-id="e0ec0-110">Dynamics 365 for Finance and Operations version 7.1, KB 4094701 Cannot enter the financial dimensions when the dimension values contain the chart of accounts delimiter</span></span>
- <span data-ttu-id="e0ec0-111">Dynamics 365 for Finance and Operations الإصدار 7.2، KB 4092967 لا يمكن اختيار مشروع فرعي كالبُعد مثلاً عندما يحتوي تنسيق مشروع فرعي على محدد أبعاد</span><span class="sxs-lookup"><span data-stu-id="e0ec0-111">Dynamics 365 for Finance and Operations version 7.2, KB 4092967 Cannot choose sub-project as dimension when sub-project format contains the dimension delimiter</span></span>

## <a name="update-delimiter"></a><span data-ttu-id="e0ec0-112">تحديث المحدد</span><span class="sxs-lookup"><span data-stu-id="e0ec0-112">Update delimiter</span></span>
<span data-ttu-id="e0ec0-113">في حالة وجود تعارض في "دليل الحسابات"، يمكن تغيير محدد دليل الحسابات وتنسيق معرف المشروع/المشروع الفرعي.</span><span class="sxs-lookup"><span data-stu-id="e0ec0-113">If there is a conflict with the Chart of Accounts, the Chart of accounts delimiter and the project/subproject ID format can be changed.</span></span> <span data-ttu-id="e0ec0-114">لا يمكن تغيير أي محددات أبعاد أخرى.</span><span class="sxs-lookup"><span data-stu-id="e0ec0-114">No other dimension delimiters can be changed.</span></span> 
- <span data-ttu-id="e0ec0-115">يمكنك تغيير محدد دليل الحسابات بعد الترقية إلى Finance and Operations في **محددات دفتر الأستاذ العام** > **دليل الحسابات والأبعاد** > **تغيير محدد**.</span><span class="sxs-lookup"><span data-stu-id="e0ec0-115">You can change the chart of accounts delimiter after upgrade to Finance and Operations in **General ledger parameters** > **Chart of accounts and dimensions** > **Change delimiter**.</span></span> 
- <span data-ttu-id="e0ec0-116">إذا كان التعارض فقط في تنسيق معرف المشروع/المشروع الفرعي، يمكنك تغيير هذه القيمة في **محددات المحاسبة وإدارة المشروع** > **عام** > **تعديل تنسيق المشروع الفرعي**.</span><span class="sxs-lookup"><span data-stu-id="e0ec0-116">If the only conflict is with the project/subproject ID format, you can change that value in **Project management and accounting parameters** > **General** > **Modify subproject format**.</span></span> 

## <a name="how-to-determine-if-your-environment-requires-updated-delimiters"></a><span data-ttu-id="e0ec0-117">كيفية تحديد ما إذا كانت البيئة الخاصة بك تتطلب محددات محدَّثة</span><span class="sxs-lookup"><span data-stu-id="e0ec0-117">How to determine if your environment requires updated delimiters</span></span> 
<span data-ttu-id="e0ec0-118">في حالة حدوث تعارض بين المحددات الموجودة في البيئة الخاصة بك التي تمت ترقيتها، تواجه عدم استقرار عند إدخال قيم في عنصر تحكم الإدخال المقسَّم أو عنصر تحكم إدخال الأبعاد.</span><span class="sxs-lookup"><span data-stu-id="e0ec0-118">If delimiters in your upgraded environment are conflicting, you may experience instability when entering values in a segmented entry control or dimension entry control.</span></span> <span data-ttu-id="e0ec0-119">ويعني هذا أنك ستحتاج دائمًا إلى استخدام عمليات بحث أو قائمة منبثقة عند إدخال مجموعات الحسابات والأبعاد.</span><span class="sxs-lookup"><span data-stu-id="e0ec0-119">This means that you will need to always use lookups or a flyout menu when entering account and dimension combinations.</span></span>
