---
title: لا يمكنك إلغاء العمل الذي يتم تشغيله على أحد المستخدمين
description: لا يمكنك إلغاء العمل الذي يتم تشغيله على أحد المستخدمين
author: perlynne
ms.date: 04/15/2021
ms.topic: troubleshooting
ms.search.form: WHSWorkTable_WHSWorkCancel, WHSWorkTableListPage_WHSWorkCancel
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2021-05-15
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: e5f6912cfb1d5be8e46b7989856af99f8a611c11
ms.sourcegitcommit: 5f5afb46431e1abd8fb6e92e0189914b598dc7fd
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 04/21/2021
ms.locfileid: "5924391"
---
# <a name="you-cant-cancel-work-that-is-on-a-user"></a><span data-ttu-id="6caa9-103">لا يمكنك إلغاء العمل الذي يتم تشغيله على أحد المستخدمين</span><span class="sxs-lookup"><span data-stu-id="6caa9-103">You can't cancel work that is on a user</span></span>

<span data-ttu-id="6caa9-104">رمز الخطأ: WAX708</span><span class="sxs-lookup"><span data-stu-id="6caa9-104">Error code: WAX708</span></span>

## <a name="symptoms"></a><span data-ttu-id="6caa9-105">العلامات</span><span class="sxs-lookup"><span data-stu-id="6caa9-105">Symptoms</span></span>

<span data-ttu-id="6caa9-106">يعرض النظام رسالة الخطأ التالية:</span><span class="sxs-lookup"><span data-stu-id="6caa9-106">The system shows the following error message:</span></span>

> <span data-ttu-id="6caa9-107">لا يمكن إلغاء عمل موجود للمستخدم.</span><span class="sxs-lookup"><span data-stu-id="6caa9-107">You cannot cancel work that is on a user.</span></span>

## <a name="cause"></a><span data-ttu-id="6caa9-108">السبب</span><span class="sxs-lookup"><span data-stu-id="6caa9-108">Cause</span></span>

<span data-ttu-id="6caa9-109">العمل مغلق من قبل مستخدم ولا يمكن إلغاؤه.</span><span class="sxs-lookup"><span data-stu-id="6caa9-109">The work is locked by a user and can't be canceled.</span></span> <span data-ttu-id="6caa9-110">لتأكيد ذلك، افتح معرّف العمل ثم افتح علامة التبويب **عام**. إذا تم قفل العمل، فسيتم تعيين حقل **حالة العمل** إلى *قيد التقدم*، وسيتم تعيين حقل **تم القفل بواسطة** إلى معرف المستخدم.</span><span class="sxs-lookup"><span data-stu-id="6caa9-110">To confirm this, open the work ID and then open the **General** tab. If the work is locked, the **Work status** field will be set to *In progress*, and the **Locked by** field will be set to a user ID.</span></span>

## <a name="resolution"></a><span data-ttu-id="6caa9-111">الدقة</span><span class="sxs-lookup"><span data-stu-id="6caa9-111">Resolution</span></span>

<span data-ttu-id="6caa9-112">لإلغاء العمل، اتبع الخطوات التالية.</span><span class="sxs-lookup"><span data-stu-id="6caa9-112">To cancel the work, follow these steps.</span></span>

1. <span data-ttu-id="6caa9-113">انتقل إلى **إدارة المستودع \> المهام الدورية \> تنظيف \> إلغاء العمل**.</span><span class="sxs-lookup"><span data-stu-id="6caa9-113">Go to **Warehouse management \> Periodic tasks \> Clean up \> Cancel work**.</span></span>
1. <span data-ttu-id="6caa9-114">في حقل **معرف العمل**، حدد معرف العمل الذي ترغب في إلغائه.</span><span class="sxs-lookup"><span data-stu-id="6caa9-114">In the **Work ID** field, specify the ID of the work that you want to cancel.</span></span>
1. <span data-ttu-id="6caa9-115">حدد **موافق**.</span><span class="sxs-lookup"><span data-stu-id="6caa9-115">Select **OK**.</span></span>
1. <span data-ttu-id="6caa9-116">حدد **نعم** لتأكيد رغبتك في إلغاء العمل.</span><span class="sxs-lookup"><span data-stu-id="6caa9-116">Select **Yes** to confirm that you want to cancel the work.</span></span>

<span data-ttu-id="6caa9-117">لمزيد من المعلومات، راجع [إلغاء عمل المستودع لمعالجة الاستثناء](../../warehousing/cancel-warehouse-work.md).</span><span class="sxs-lookup"><span data-stu-id="6caa9-117">For more information, see [Cancel warehouse work for exception handling](../../warehousing/cancel-warehouse-work.md).</span></span>
