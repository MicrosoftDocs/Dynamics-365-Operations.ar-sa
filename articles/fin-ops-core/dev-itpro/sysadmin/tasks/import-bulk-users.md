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
ms.author: maertenm
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: cb2c316465f8c6964a562e92ce0a2233b37d38fe
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 09/27/2019
ms.locfileid: "2180888"
---
# <a name="import-users-in-bulk"></a><span data-ttu-id="e284d-103">استيراد المستخدمين بشكل مجمع</span><span class="sxs-lookup"><span data-stu-id="e284d-103">Import users in bulk</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="e284d-104">يمكن استخدام هذا الإجراء من قبل مسؤولي النظام لاستيراد عدد كبير من المستخدمين من خدمة Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="e284d-104">This procedure can be used by system administrators to import a large number of users from Azure Active Directory.</span></span>


## <a name="run-as-a-batch-job"></a><span data-ttu-id="e284d-105">يمكن تشغيله كوظيفة دفعية‬</span><span class="sxs-lookup"><span data-stu-id="e284d-105">Run as a batch job</span></span>
1. <span data-ttu-id="e284d-106">انتقل إلى إدارة النظام > المستخدمين > المستخدمين.</span><span class="sxs-lookup"><span data-stu-id="e284d-106">Go to System administration > Users > Users.</span></span>
2. <span data-ttu-id="e284d-107">انقر فوق "استيراد دُفعة‬".</span><span class="sxs-lookup"><span data-stu-id="e284d-107">Click Batch import.</span></span>
3. <span data-ttu-id="e284d-108">وسّع المقطع "تشغيل في الخلفية‬‬".</span><span class="sxs-lookup"><span data-stu-id="e284d-108">Expand the Run in the background section.</span></span>
4. <span data-ttu-id="e284d-109">حدد "نعم" في حقل "معالجة الدُفعات‬".</span><span class="sxs-lookup"><span data-stu-id="e284d-109">Select Yes in the Batch processing field.</span></span>
5. <span data-ttu-id="e284d-110">في حقل "وصف المهمة"، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="e284d-110">In the Task description field, type a value.</span></span>
6. <span data-ttu-id="e284d-111">في الحقل "مجموعة الدُفعات‬"، أدخل قيمة أو حددها.</span><span class="sxs-lookup"><span data-stu-id="e284d-111">In the Batch group field, enter or select a value.</span></span>
    * <span data-ttu-id="e284d-112">هذه خطوة اختيارية.</span><span class="sxs-lookup"><span data-stu-id="e284d-112">This is an optional step.</span></span>  
7. <span data-ttu-id="e284d-113">حدد "نعم" في الحقل "خاص‬".</span><span class="sxs-lookup"><span data-stu-id="e284d-113">Select Yes in the Private field.</span></span>
    * <span data-ttu-id="e284d-114">هذه خطوة اختيارية.</span><span class="sxs-lookup"><span data-stu-id="e284d-114">This is an optional step.</span></span>  
8. <span data-ttu-id="e284d-115">حدد "نعم" في حقل "وظيفة هامة‬‬".</span><span class="sxs-lookup"><span data-stu-id="e284d-115">Select Yes in the Critical Job field.</span></span>
    * <span data-ttu-id="e284d-116">هذه خطوة اختيارية.</span><span class="sxs-lookup"><span data-stu-id="e284d-116">This is an optional step.</span></span>  
9. <span data-ttu-id="e284d-117">في الحقل "فئة المراقبة‬"، حدد خيارًا.</span><span class="sxs-lookup"><span data-stu-id="e284d-117">In the Monitoring category field, select an option.</span></span>
10. <span data-ttu-id="e284d-118">انقر فوق "موافق".</span><span class="sxs-lookup"><span data-stu-id="e284d-118">Click OK.</span></span>

## <a name="run-in-a-sandbox-environment"></a><span data-ttu-id="e284d-119">التشغيل في بيئة وضع الحماية</span><span class="sxs-lookup"><span data-stu-id="e284d-119">Run in a sandbox environment</span></span>
1. <span data-ttu-id="e284d-120">انقر فوق "استيراد دُفعة‬".</span><span class="sxs-lookup"><span data-stu-id="e284d-120">Click Batch import.</span></span>
2. <span data-ttu-id="e284d-121">انقر فوق "موافق".</span><span class="sxs-lookup"><span data-stu-id="e284d-121">Click OK.</span></span>

