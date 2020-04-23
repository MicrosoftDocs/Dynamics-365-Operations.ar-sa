---
title: تسجيل برنامج تسجيل دخول وتسجيل خروج السائق لموعد
description: يوضح هذا الإجراء كيفية تسجيل عمليات تسجيل دخول السائق وخروجه.
author: ShylaThompson
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TMSDriverLogListPage, TMSDriverCheckIn
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 2baa5e6bce3fa16199e97bf87ea03fa9a55a681a
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 04/02/2020
ms.locfileid: "3206140"
---
# <a name="register-driver-check-in-and-check-out-for-an-appointment"></a><span data-ttu-id="9ee4c-103">تسجيل برنامج تسجيل دخول وتسجيل خروج السائق لموعد</span><span class="sxs-lookup"><span data-stu-id="9ee4c-103">Register driver check-in and check-out for an appointment</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="9ee4c-104">يُظهر هذا الإجراء كيفية تسجيل دخول السائق وكيفية تسجيل خروج السائق. ينفذ هذا الإجراء عادةً منسق النقل.</span><span class="sxs-lookup"><span data-stu-id="9ee4c-104">This procedure shows how to register a driver check-in and a driver check-out. This is typically done by a transportation coordinator.</span></span> <span data-ttu-id="9ee4c-105">يمكنك تنفيذ هذا الإجراء في شركة بيانات العرض التوضيحي USMF.</span><span class="sxs-lookup"><span data-stu-id="9ee4c-105">You can use this procedure in the USMF demo data company.</span></span> <span data-ttu-id="9ee4c-106">قبل البدء، يجب أن إعداد موعد لحمولة.</span><span class="sxs-lookup"><span data-stu-id="9ee4c-106">Before you start, there must be an appointment set up for a load.</span></span> <span data-ttu-id="9ee4c-107">لإنشاء موعد، يمكنك تشغيل الإجراء "إعداد موعد لحمولة" كشرط مسبق.</span><span class="sxs-lookup"><span data-stu-id="9ee4c-107">To create an appointment, you can run the "Set up an appointment for a load" procedure as a prerequisite.</span></span>


## <a name="select-an-appointment"></a><span data-ttu-id="9ee4c-108">تحديد موعد</span><span class="sxs-lookup"><span data-stu-id="9ee4c-108">Select an appointment</span></span>
1. <span data-ttu-id="9ee4c-109">انتقل إلى إدارة النقل > التخطيط > جدولة موعد الرصيف > تسجيل دخول السائق وتسجيل خروجه‬.</span><span class="sxs-lookup"><span data-stu-id="9ee4c-109">Go to Transportation management > Planning > Dock appointment scheduling > Driver check-in and check-out.</span></span>
2. <span data-ttu-id="9ee4c-110">حدد موعدًا.</span><span class="sxs-lookup"><span data-stu-id="9ee4c-110">Select an appointment.</span></span>

## <a name="register-driver-check-in"></a><span data-ttu-id="9ee4c-111">تسجيل عملية تسجيل دخول السائق</span><span class="sxs-lookup"><span data-stu-id="9ee4c-111">Register driver check-in</span></span>
1. <span data-ttu-id="9ee4c-112">انقر فوق "تسجيل دخول السائق".</span><span class="sxs-lookup"><span data-stu-id="9ee4c-112">Click Driver check-in.</span></span>
2. <span data-ttu-id="9ee4c-113">في حقل "‏‫رقم العربة الملحقة‬‬"، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="9ee4c-113">In the Trailer number field, type a value.</span></span>
3. <span data-ttu-id="9ee4c-114">في الحقل "اسم السائق"، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="9ee4c-114">In the Driver name field, type a value.</span></span>
4. <span data-ttu-id="9ee4c-115">في الحقل "‏رخصة السائق"، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="9ee4c-115">In the Driver license field, type a value.</span></span>
5. <span data-ttu-id="9ee4c-116">انقر فوق "موافق".</span><span class="sxs-lookup"><span data-stu-id="9ee4c-116">Click OK.</span></span>

## <a name="register-driver-check-out"></a><span data-ttu-id="9ee4c-117">تسجيل عملية تسجيل خروج السائق</span><span class="sxs-lookup"><span data-stu-id="9ee4c-117">Register driver check-out</span></span>
1. <span data-ttu-id="9ee4c-118">انقر فوق "تسجيل خروج السائق".</span><span class="sxs-lookup"><span data-stu-id="9ee4c-118">Click Driver check-out.</span></span>
2. <span data-ttu-id="9ee4c-119">انقر فوق "موافق".</span><span class="sxs-lookup"><span data-stu-id="9ee4c-119">Click OK.</span></span>

