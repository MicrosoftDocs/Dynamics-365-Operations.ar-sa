---
title: لا يسمح ملف تعريف الموقع بالمخزون السالب، ولكن يتم السماح بالمخزون المتوافر السالب
description: يتم تعيين خيار السماح بالمخزون السالب لملف تعريف الموقع على لا، لكن النظام لا يزال يسمح بالمخزون المتوافر السالب.
author: niwang
ms.date: 4/11/2021
ms.topic: troubleshooting
ms.search.form: WHSLocationProfile
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: shawan
ms.search.validFrom: 2021-04-11
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: 356d2dd7853bf93250e14eb9bd28a8a145794584
ms.sourcegitcommit: c011a2ef66b38e71ddaf003f7d243677bb2707c5
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 05/12/2021
ms.locfileid: "6026233"
---
# <a name="location-profile-disallows-negative-inventory-but-negative-on-hand-inventory-is-permitted"></a><span data-ttu-id="0504d-103">لا يسمح ملف تعريف الموقع بالمخزون السالب، ولكن يتم السماح بالمخزون المتوافر السالب</span><span class="sxs-lookup"><span data-stu-id="0504d-103">Location profile disallows negative inventory, but negative on-hand inventory is permitted</span></span>

<span data-ttu-id="0504d-104">رقم KB: 4613622</span><span class="sxs-lookup"><span data-stu-id="0504d-104">KB number: 4613622</span></span>

## <a name="symptoms"></a><span data-ttu-id="0504d-105">العلامات</span><span class="sxs-lookup"><span data-stu-id="0504d-105">Symptoms</span></span>

<span data-ttu-id="0504d-106">يتم تعيين خيار **السماح بالمخزون السالب** لملف تعريف الموقع على *لا*، لكن النظام لا يزال يسمح بالمخزون المتوافر السالب.</span><span class="sxs-lookup"><span data-stu-id="0504d-106">The **Allow negative inventory** option for the location profile is set to *No*, but the system still allows negative on-hand inventory.</span></span>

## <a name="example-scenario"></a><span data-ttu-id="0504d-107">سيناريو كمثال</span><span class="sxs-lookup"><span data-stu-id="0504d-107">Example scenario</span></span>

<span data-ttu-id="0504d-108">بالنسبة للحركات التنظيمية الحكومية، يجب أن يكون النظام قادرًا على تسجيل المخزون السالب للخسائر الدفترية.</span><span class="sxs-lookup"><span data-stu-id="0504d-108">For government-regulated transactions, the system must be able to record negative inventory to book losses.</span></span> <span data-ttu-id="0504d-109">إنك ترغب في أن يكون الصنف قادرًا على إظهار المخزون السالب، ولكن في المواقع المحددة فقط، مثل الخزانات.</span><span class="sxs-lookup"><span data-stu-id="0504d-109">You want an item to be able to show negative inventory, but only in designated locations, such as tanks.</span></span> <span data-ttu-id="0504d-110">ومع ذلك، إذا كانت مجموعة نماذج الصنف تتيح المخزون السالب، فإنك تجد أنه لا يهم ما إذا كان الموقع قد تم تعيينه للسماح بالمخزون السالب أم لا.</span><span class="sxs-lookup"><span data-stu-id="0504d-110">However, if the item model group allows negative inventory, you find that it doesn't matter whether the location is set to allow negative inventory.</span></span> <span data-ttu-id="0504d-111">في حالة إعداد الصنف بحيث لا يتم السماح بالمخزون السالب، فلا يهم كيفية إعداد ملف تعريف الموقع.</span><span class="sxs-lookup"><span data-stu-id="0504d-111">If the item is set up so that negative inventory isn't allowed, it doesn't matter how the location profile is set up.</span></span>

## <a name="resolution"></a><span data-ttu-id="0504d-112">الدقة</span><span class="sxs-lookup"><span data-stu-id="0504d-112">Resolution</span></span>

<span data-ttu-id="0504d-113">يتم تطبيق الإعداد **السماح بالمخزون السالب** من ملف تعريف الموقع فقط على عمليات المستودع، مثل الانتقاء.</span><span class="sxs-lookup"><span data-stu-id="0504d-113">The **Allow negative inventory** setting from the location profile applies only to warehouse processes, such as picking.</span></span> <span data-ttu-id="0504d-114">ومع ذلك، فإن مجموعات نماذج الأصناف التي تم تعيينها للسماح بالمخزون السالب تؤثر على كافة العمليات من الوحدات النمطية لإدارة المخزون وإدارة المستودع، ولن يتجاوز ملف تعريف الموقع الإعداد.</span><span class="sxs-lookup"><span data-stu-id="0504d-114">However, item model groups that are set to allow negative inventory affect all processes from the Inventory management and Warehouse management modules, and the location profile won't override the setting.</span></span>

<span data-ttu-id="0504d-115">يمكنك التحكم في ما إذا كان مسموحًا لمستودع بأن تحتوي على مخزون سالب أم لا.</span><span class="sxs-lookup"><span data-stu-id="0504d-115">You can control whether a warehouse is allowed to carry negative inventory.</span></span> <span data-ttu-id="0504d-116">قم بتعيين مجموعات نموذج الصنف الخاص بك لعدم السماح بالمخزون الفعلي السالب، وتعيين المستودع المرتبط فقط للسماح بالمخزون السالب.</span><span class="sxs-lookup"><span data-stu-id="0504d-116">Set your item model groups to disallow negative physical inventory, and set only the relevant warehouse to allow negative inventory.</span></span>
