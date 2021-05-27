---
title: يحدث خطأ عند تحديد الموقع أثناء تسجيل قائمة الانتقاء
description: يحدث خطأ عند تحديد الموقع أثناء تسجيل قائمة الانتقاء.
author: perlynne
ms.date: 4/11/2021
ms.topic: troubleshooting
ms.search.form: WMSPickingRegistration
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2021-04-11
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: b7fc579821f9a80d94aea949fcc0301b9d8f6935
ms.sourcegitcommit: c011a2ef66b38e71ddaf003f7d243677bb2707c5
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 05/12/2021
ms.locfileid: "6026219"
---
# <a name="an-error-occurs-when-the-location-is-selected-during-picking-list-registration"></a><span data-ttu-id="acc91-103">يحدث خطأ عند تحديد الموقع أثناء تسجيل قائمة الانتقاء</span><span class="sxs-lookup"><span data-stu-id="acc91-103">An error occurs when the location is selected during picking list registration</span></span>

<span data-ttu-id="acc91-104">رقم KB: 4613106</span><span class="sxs-lookup"><span data-stu-id="acc91-104">KB number: 4613106</span></span>

## <a name="symptoms"></a><span data-ttu-id="acc91-105">العلامات</span><span class="sxs-lookup"><span data-stu-id="acc91-105">Symptoms</span></span>

<span data-ttu-id="acc91-106">تحدث هذه المشكلة في حالة تكوين النظام الخاص بك لحجز أوامر المبيعات تلقائيًا.</span><span class="sxs-lookup"><span data-stu-id="acc91-106">This issue occurs when your system is configured to automatically reserve sales orders.</span></span> <span data-ttu-id="acc91-107">إذا حاولت تحديد موقع لبند تسجيل قائمة الانتقاء، فإنك تتلقي رسالة الخطأ التالية عند استخدام عمليات الحجز لإدارة المستودع (WMS):</span><span class="sxs-lookup"><span data-stu-id="acc91-107">If you try to select the location for a picking list registration line, you receive the following error message when you use warehouse management (WMS) reservation processes:</span></span>

> <span data-ttu-id="acc91-108">لا يمكن تحديث الكمية بالأبعاد الجديدة</span><span class="sxs-lookup"><span data-stu-id="acc91-108">Can't update quantity with new dimensions</span></span>

<span data-ttu-id="acc91-109">قد تحدث هذه المشكلة نظرًا لعدم وجود مخزون فعلي كافي في موقع محدد.</span><span class="sxs-lookup"><span data-stu-id="acc91-109">This issue can occur because you don't have enough on-hand inventory at a specified location.</span></span>

## <a name="resolution"></a><span data-ttu-id="acc91-110">الدقة</span><span class="sxs-lookup"><span data-stu-id="acc91-110">Resolution</span></span>

<span data-ttu-id="acc91-111">يعمل النظام كما هو مصمم.</span><span class="sxs-lookup"><span data-stu-id="acc91-111">The system is behaving as designed.</span></span>

<span data-ttu-id="acc91-112">في السيناريوهات التي تستخدم فيها عملية الحجز على مستوى المستودع، إذا لم يتم حجز المخزون الفعلي على كافة مستويات أبعاد المخزون، ولم يكن لديك مخزون فعلي كاف في موقع محدد، فإننا نوصي باستخدام عملية الحجز اليدوي من بند الانتقاء.</span><span class="sxs-lookup"><span data-stu-id="acc91-112">In scenarios where you use the warehouse-level reservation process, if the on-hand inventory won't be reserved on all inventory dimension levels, and you don't have enough on-hand inventory at a specified location, we recommend that you use the manual reservation process from the picking line.</span></span> <span data-ttu-id="acc91-113">ويمكنك بعد ذلك استخدام الوظيفة *حجز دفعة* لتوزيع الحجوزات الأدنى، مثل الموقع، لكافة الكميات الفعلية المتاحة.</span><span class="sxs-lookup"><span data-stu-id="acc91-113">You can then use the *Reserve lot* function to distribute the lower reservations, such as location, for all the available on-hand quantities.</span></span>
