---
title: استيراد المستخدمين بشكل مجمع
description: يمكن استخدام هذا الإجراء من قبل مسؤولي النظام لاستيراد عدد كبير من المستخدمين من خدمة Azure Active Directory.
author: maertenm
manager: AnnBe
ms.date: 07/07/2017
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: sericks
ms.search.scope: Operations
ms.search.region: Global
ms.author: sericks
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: fa86d408727ecf2127308070fda592ff6a1fccf4
ms.sourcegitcommit: 708ca25687a4e48271cdcd6d2d22d99fb94cf140
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 10/10/2020
ms.locfileid: "3982444"
---
# <a name="import-users-in-bulk"></a><span data-ttu-id="88bb6-103">استيراد المستخدمين بشكل مجمع</span><span class="sxs-lookup"><span data-stu-id="88bb6-103">Import users in bulk</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="88bb6-104">يمكن استخدام هذا الإجراء من قبل مسؤولي النظام لاستيراد عدد كبير من المستخدمين من خدمة Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="88bb6-104">This procedure can be used by system administrators to import a large number of users from Azure Active Directory.</span></span>


## <a name="run-as-a-batch-job"></a><span data-ttu-id="88bb6-105">يمكن تشغيله كوظيفة دفعية‬</span><span class="sxs-lookup"><span data-stu-id="88bb6-105">Run as a batch job</span></span>
1. <span data-ttu-id="88bb6-106">انتقل إلى إدارة النظام > المستخدمين > المستخدمين.</span><span class="sxs-lookup"><span data-stu-id="88bb6-106">Go to System administration > Users > Users.</span></span>
2. <span data-ttu-id="88bb6-107">انقر فوق "استيراد دُفعة‬".</span><span class="sxs-lookup"><span data-stu-id="88bb6-107">Click Batch import.</span></span>
3. <span data-ttu-id="88bb6-108">وسّع المقطع "تشغيل في الخلفية‬‬".</span><span class="sxs-lookup"><span data-stu-id="88bb6-108">Expand the Run in the background section.</span></span>
4. <span data-ttu-id="88bb6-109">حدد "نعم" في حقل "معالجة الدُفعات‬".</span><span class="sxs-lookup"><span data-stu-id="88bb6-109">Select Yes in the Batch processing field.</span></span>
5. <span data-ttu-id="88bb6-110">في حقل "وصف المهمة"، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="88bb6-110">In the Task description field, type a value.</span></span>
6. <span data-ttu-id="88bb6-111">في الحقل "مجموعة الدُفعات‬"، أدخل قيمة أو حددها.</span><span class="sxs-lookup"><span data-stu-id="88bb6-111">In the Batch group field, enter or select a value.</span></span>
    * <span data-ttu-id="88bb6-112">هذه خطوة اختيارية.</span><span class="sxs-lookup"><span data-stu-id="88bb6-112">This is an optional step.</span></span>  
7. <span data-ttu-id="88bb6-113">حدد "نعم" في الحقل "خاص‬".</span><span class="sxs-lookup"><span data-stu-id="88bb6-113">Select Yes in the Private field.</span></span>
    * <span data-ttu-id="88bb6-114">هذه خطوة اختيارية.</span><span class="sxs-lookup"><span data-stu-id="88bb6-114">This is an optional step.</span></span>  
8. <span data-ttu-id="88bb6-115">حدد "نعم" في حقل "وظيفة هامة‬‬".</span><span class="sxs-lookup"><span data-stu-id="88bb6-115">Select Yes in the Critical Job field.</span></span>
    * <span data-ttu-id="88bb6-116">هذه خطوة اختيارية.</span><span class="sxs-lookup"><span data-stu-id="88bb6-116">This is an optional step.</span></span>  
9. <span data-ttu-id="88bb6-117">في الحقل "فئة المراقبة‬"، حدد خيارًا.</span><span class="sxs-lookup"><span data-stu-id="88bb6-117">In the Monitoring category field, select an option.</span></span>
10. <span data-ttu-id="88bb6-118">انقر فوق "موافق".</span><span class="sxs-lookup"><span data-stu-id="88bb6-118">Click OK.</span></span>

## <a name="run-in-a-sandbox-environment"></a><span data-ttu-id="88bb6-119">التشغيل في بيئة وضع الحماية</span><span class="sxs-lookup"><span data-stu-id="88bb6-119">Run in a sandbox environment</span></span>
1. <span data-ttu-id="88bb6-120">انقر فوق "استيراد دُفعة‬".</span><span class="sxs-lookup"><span data-stu-id="88bb6-120">Click Batch import.</span></span>
2. <span data-ttu-id="88bb6-121">انقر فوق "موافق".</span><span class="sxs-lookup"><span data-stu-id="88bb6-121">Click OK.</span></span>

