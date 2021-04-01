---
title: إعداد مصاريف الموزع الإضافية والأصول الإضافية
description: يوضح هذا الإجراء كيفية إنشاء سجل رئيسي إضافي‬ للموزع واستخدامه لإنشاء رسوم الموزِّع الإضافي‬.
author: ShylaThompson
manager: tfehr
ms.date: 11/11/2016
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TMSCarrierAccessorial,TMSAccessorialMaster, TMSHubAccessorial
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Distribution
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: cb2e9125c7a38d1dc5e6866a056fb71f25e40928
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 02/15/2021
ms.locfileid: "5233669"
---
# <a name="set-up-hub-accessorial-charges-and-accessorial-masters"></a><span data-ttu-id="0bc95-103">إعداد مصاريف الموزع الإضافية والأصول الإضافية</span><span class="sxs-lookup"><span data-stu-id="0bc95-103">Set up hub accessorial charges and accessorial masters</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="0bc95-104">يوضح هذا الإجراء كيفية إنشاء سجل رئيسي إضافي‬ للموزع واستخدامه لإنشاء رسوم الموزِّع الإضافي‬.</span><span class="sxs-lookup"><span data-stu-id="0bc95-104">This procedure shows how to create an accessorial master for a hub and use that master to create a hub accessorial charge.</span></span> <span data-ttu-id="0bc95-105">يستخدم هذا الإجراء مجموعة بيانات USMF.</span><span class="sxs-lookup"><span data-stu-id="0bc95-105">The procedure uses the USMF dataset.</span></span> <span data-ttu-id="0bc95-106">عادة ما يتم تنفيذ هذا الإعداد عن طريق منسق نقل.</span><span class="sxs-lookup"><span data-stu-id="0bc95-106">This set up will typically be done by a transportation coordinator.</span></span>


## <a name="set-up-a-hub-master"></a><span data-ttu-id="0bc95-107">إعداد الخطط الرئيسية</span><span class="sxs-lookup"><span data-stu-id="0bc95-107">Set up a hub master</span></span>
1. <span data-ttu-id="0bc95-108">انتقل إلى إدارة النقل > إعداد > التقييم‬ > الأصول الإضافية.</span><span class="sxs-lookup"><span data-stu-id="0bc95-108">Go to Transportation management > Setup > Rating > Accessorial masters.</span></span>
2. <span data-ttu-id="0bc95-109">انقر فوق "جديد".</span><span class="sxs-lookup"><span data-stu-id="0bc95-109">Click New.</span></span>
3. <span data-ttu-id="0bc95-110">في الحقل "الأصول الإضافية‬"، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="0bc95-110">In the Accessorial master field, type a value.</span></span>
4. <span data-ttu-id="0bc95-111">في حقل "الاسم"، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="0bc95-111">In the Name field, type a value.</span></span>
5. <span data-ttu-id="0bc95-112">في الحقل "نوع الرسوم الإضافية‬"، حدد "الموزع".</span><span class="sxs-lookup"><span data-stu-id="0bc95-112">In the Accessorial type field, select 'Hub'.</span></span>
6. <span data-ttu-id="0bc95-113">انقر فوق "حفظ".</span><span class="sxs-lookup"><span data-stu-id="0bc95-113">Click Save.</span></span>
7. <span data-ttu-id="0bc95-114">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="0bc95-114">Close the page.</span></span>

## <a name="set-up-a-hub-accessorial-charge"></a><span data-ttu-id="0bc95-115">إعداد رسوم الموزِّع الإضافي‬</span><span class="sxs-lookup"><span data-stu-id="0bc95-115">Set up a hub accessorial charge</span></span>
1. <span data-ttu-id="0bc95-116">انتقل إلى إدارة النقل > إعداد > التقييم‬ > تكاليف الموزِّع الإضافية‬.</span><span class="sxs-lookup"><span data-stu-id="0bc95-116">Go to Transportation management > Setup > Rating > Hub accessorial charges.</span></span>
2. <span data-ttu-id="0bc95-117">انقر فوق "جديد".</span><span class="sxs-lookup"><span data-stu-id="0bc95-117">Click New.</span></span>
3. <span data-ttu-id="0bc95-118">في الحقل "معرف الموزِّع الإضافي‬‬"، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="0bc95-118">In the Hub accessorial ID field, type a value.</span></span>
4. <span data-ttu-id="0bc95-119">في الحقل "الموزِّع‬"، انقر فوق زر القائمة المنسدلة لفتح البحث.</span><span class="sxs-lookup"><span data-stu-id="0bc95-119">In the Hub field, click the drop-down button to open the lookup.</span></span>
5. <span data-ttu-id="0bc95-120">في القائمة، قم بالبحث عن السجل المطلوب وحدده.</span><span class="sxs-lookup"><span data-stu-id="0bc95-120">In the list, find and select the desired record.</span></span>
6. <span data-ttu-id="0bc95-121">في الحقل "موضع الموزِّع‬"، حدد خيارًا.</span><span class="sxs-lookup"><span data-stu-id="0bc95-121">In the Hub position field, select an option.</span></span>
    * <span data-ttu-id="0bc95-122">يمكنك إنشاء التكلفة كانتقاء أو تسليم.</span><span class="sxs-lookup"><span data-stu-id="0bc95-122">You can either create the charge as a pickup or drop-off.</span></span> <span data-ttu-id="0bc95-123">بحسب اختيارك، سيتم تطبيق التكلفة على جزء النقل المناظر على مسارك.</span><span class="sxs-lookup"><span data-stu-id="0bc95-123">Depending on your selection the charge will be applied to the corresponding transportation segment on your route.</span></span>  
7. <span data-ttu-id="0bc95-124">في الحقل "الأصل الإضافي‬‬"، انقر فوق زر القائمة المنسدلة لفتح البحث.</span><span class="sxs-lookup"><span data-stu-id="0bc95-124">In the Accessorial master field, click the drop-down button to open the lookup.</span></span>
8. <span data-ttu-id="0bc95-125">في القائمة، انقر فوق الارتباط في الصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="0bc95-125">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="0bc95-126">حدد السجل الرئيسي الذي أنشأته للتوّ.</span><span class="sxs-lookup"><span data-stu-id="0bc95-126">Select the master you just created.</span></span>  
9. <span data-ttu-id="0bc95-127">انقر فوق "حفظ".</span><span class="sxs-lookup"><span data-stu-id="0bc95-127">Click Save.</span></span>
10. <span data-ttu-id="0bc95-128">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="0bc95-128">Close the page.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]