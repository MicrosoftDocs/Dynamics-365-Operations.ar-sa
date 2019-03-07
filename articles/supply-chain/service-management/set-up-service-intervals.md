---
title: إعداد الفواصل الزمنية لخدمة
description: تشير فترة الخدمة إلى تكرار إنشاء بنود أمر الخدمة من أجل بنود اتفاقية الخدمة عند قيامك بإنشاء أوامر الخدمة.
author: ShylaThompson
manager: AnnBe
ms.date: 02/20/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SMAAgreementinterval
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: ShylaThompson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: d9203b01f578779d45d63c18d1c1afd2fe59125b
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 01/29/2019
ms.locfileid: "365812"
---
# <a name="set-up-service-intervals"></a><span data-ttu-id="7a8f5-103">إعداد الفواصل الزمنية لخدمة</span><span class="sxs-lookup"><span data-stu-id="7a8f5-103">Set up service intervals</span></span>  

[!include [banner](../includes/banner.md)]

<span data-ttu-id="7a8f5-104">تشير فترة الخدمة إلى تكرار إنشاء بنود أمر الخدمة من أجل بنود اتفاقية الخدمة عند قيامك بإنشاء أوامر الخدمة.</span><span class="sxs-lookup"><span data-stu-id="7a8f5-104">Service interval indicates the frequency with which service order lines are created for service agreement lines when you create service orders.</span></span>

1. <span data-ttu-id="7a8f5-105">انقر فوق **إدارة الخدمة** \> **الإعداد** \> **اتفاقيات الخدمة** \> **فترات الخدمة‬**.</span><span class="sxs-lookup"><span data-stu-id="7a8f5-105">Click **Service management** \> **Setup** \> **Service agreements** \> **Service intervals**.</span></span>
2. <span data-ttu-id="7a8f5-106">قم بإنشاء فترة خدمة جديدة.</span><span class="sxs-lookup"><span data-stu-id="7a8f5-106">Create a new service interval.</span></span>
3. <span data-ttu-id="7a8f5-107">أدخل معرّف فترة الخدمة ووصفها.</span><span class="sxs-lookup"><span data-stu-id="7a8f5-107">Enter the ID and description of the service interval.</span></span>
4. <span data-ttu-id="7a8f5-108">في حقل **النطاق**، حدد النطاق.</span><span class="sxs-lookup"><span data-stu-id="7a8f5-108">In the **Range** field, select the range.</span></span>
5. <span data-ttu-id="7a8f5-109">في حقل **التكرار‬**، اكتب التكرار‬.</span><span class="sxs-lookup"><span data-stu-id="7a8f5-109">In the **Frequency** field, type the frequency.</span></span> <span data-ttu-id="7a8f5-110">يعتبر التكرار العامل الذي يجب ضرب النطاق فيه للحصول على فترة اتفاقية الخدمة.</span><span class="sxs-lookup"><span data-stu-id="7a8f5-110">The frequency is the factor by which you must multiply the range to obtain the interval for a service agreement.</span></span>
6. <span data-ttu-id="7a8f5-111">اضغط على **Alt+S** لحفظ فترة الخدمة.</span><span class="sxs-lookup"><span data-stu-id="7a8f5-111">Press **Alt+S** to save the service interval.</span></span>

## <a name="example"></a><span data-ttu-id="7a8f5-112">مثال</span><span class="sxs-lookup"><span data-stu-id="7a8f5-112">Example</span></span>

<span data-ttu-id="7a8f5-113">إنك تريد إنشاء فترة خدمة تبلغ 10 أيام.</span><span class="sxs-lookup"><span data-stu-id="7a8f5-113">You want to create a service interval of 10 days.</span></span>

<span data-ttu-id="7a8f5-114">**إنشاء فترة خدمة تبلغ 10 أيام**</span><span class="sxs-lookup"><span data-stu-id="7a8f5-114">**Create a 10-day service interval**</span></span>

1. <span data-ttu-id="7a8f5-115">انقر فوق **إدارة الخدمة** \> **الإعداد** \> **اتفاقيات الخدمة** \> **فترات الخدمة‬**.</span><span class="sxs-lookup"><span data-stu-id="7a8f5-115">Click **Service management** \> **Setup** \> **Service agreements** \> **Service intervals**.</span></span>
2. <span data-ttu-id="7a8f5-116">قم بإنشاء فترة خدمة جديدة.</span><span class="sxs-lookup"><span data-stu-id="7a8f5-116">Create a new service interval.</span></span>
3. <span data-ttu-id="7a8f5-117">أدخل معرّف فترة الخدمة ووصفها.</span><span class="sxs-lookup"><span data-stu-id="7a8f5-117">Enter the ID and description of the service interval.</span></span>
4. <span data-ttu-id="7a8f5-118">في حقل **النطاق**، حدد **يوميًا**.</span><span class="sxs-lookup"><span data-stu-id="7a8f5-118">In the **Range** field, select **Daily**.</span></span>
5. <span data-ttu-id="7a8f5-119">في حقل **التكرار**، اكتب 10.</span><span class="sxs-lookup"><span data-stu-id="7a8f5-119">In the **Frequency** field, type 10.</span></span>
6. <span data-ttu-id="7a8f5-120">اضغط على **Alt+S** لحفظ فترة الخدمة.</span><span class="sxs-lookup"><span data-stu-id="7a8f5-120">Press **Alt+S** to save the service interval.</span></span>

## <a name="related-topics"></a><span data-ttu-id="7a8f5-121">مواضيع مرتبطة</span><span class="sxs-lookup"><span data-stu-id="7a8f5-121">Related topics</span></span>

[<span data-ttu-id="7a8f5-122">‏‏فترات الخدمة </span><span class="sxs-lookup"><span data-stu-id="7a8f5-122">Service intervals</span></span>](service-intervals.md)  
