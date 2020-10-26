---
title: إخفاء أوضاع التسليم بدون ناقل من خيارات الشحنة في نقطة البيع
description: يصف هذا الموضوع خيار التكوين الذي يمكنه منع أوضاع التسليم بدون ناقل من الظهور للتحديد عند إنشاء أوامر الشحن في التطبيق عند نقطه البيع (POS).
author: hhainesms
manager: annbe
ms.date: 10/24/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-retail
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Retail, Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: hhaines
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.7
ms.openlocfilehash: 38d57ed5f8d2b8725cd11156f0135988bb76e047
ms.sourcegitcommit: 708ca25687a4e48271cdcd6d2d22d99fb94cf140
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 10/10/2020
ms.locfileid: "3982979"
---
# <a name="hide-non-carrier-delivery-modes-from-the-shipping-options-in-pos"></a><span data-ttu-id="9dc2e-103">إخفاء أوضاع التسليم بدون ناقل من خيارات الشحن في نقطة البيع</span><span class="sxs-lookup"><span data-stu-id="9dc2e-103">Hide non-carrier delivery modes from the shipping options in POS</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="9dc2e-104">يصف هذا الموضوع خيار التكوين المتاح لتطبيق نقطه البيع (POS).</span><span class="sxs-lookup"><span data-stu-id="9dc2e-104">This topic describes a configuration option that is available for the point of sale (POS) application.</span></span> <span data-ttu-id="9dc2e-105">يقوم خيار التكوين هذا بتغيير سلوك تحديد وضع التسليم عند إنشاء أوامر الشحن في نقطه البيع (POS).</span><span class="sxs-lookup"><span data-stu-id="9dc2e-105">This configuration option changes the behavior for the selection of a mode of delivery when shipment orders are created in POS.</span></span>

<span data-ttu-id="9dc2e-106">عندما يقوم المستخدمون بإنشاء أوامر شحن عميل في نقطه البيع (POS)، يمكنهم تحديد وضع التسليم للشحنة.</span><span class="sxs-lookup"><span data-stu-id="9dc2e-106">When users create customer shipment orders in POS, they can select a mode of delivery for the shipment.</span></span> <span data-ttu-id="9dc2e-107">تتوفر هذه الوظيفة بغض النظر عما إذا كان الأمر يتم شحنه بالكامل أو إذا كانت البنود المحددة فقط.</span><span class="sxs-lookup"><span data-stu-id="9dc2e-107">This functionality is available regardless of whether the whole order is being shipped or only selected lines.</span></span>

<span data-ttu-id="9dc2e-108">وبشكل افتراضي، يظهر مربع الحوار عند تحديد وضع التسليم كافة أوضاع التسليم الصالحة لمجموعة القناة والصنف وعنوان التسليم.</span><span class="sxs-lookup"><span data-stu-id="9dc2e-108">By default, the dialog box where a mode of delivery is selected shows all the valid modes of delivery for the combination of a channel, an item, and a delivery address.</span></span> <span data-ttu-id="9dc2e-109">يتم تحديد أوضاع التسليم هذه في صفحة **أوضاع التسليم** في المراكز الرئيسية ( **المبيعات والتسويق \> الإعداد \> التوزيع \> أوضاع التسليم** ).</span><span class="sxs-lookup"><span data-stu-id="9dc2e-109">These modes of delivery are defined on the **Modes of delivery** page in Headquarters ( **Sales and marketing \> Setup \> Distribution \> Modes of delivery** ).</span></span> <span data-ttu-id="9dc2e-110">قد تظهر أيضًا أوضاع التسليم "بدون ناقل"، مثل **تنفيذ** أو **التقاط** ، للتحديد في مربع الحوار.</span><span class="sxs-lookup"><span data-stu-id="9dc2e-110">"Non-carrier" modes of delivery, such as **Carryout** or **Pickup** , might also appear for selection in the dialog box.</span></span>

<span data-ttu-id="9dc2e-111">ومع ذلك، تمت إضافة ميزة تتيح لك إخفاء أوضاع التسليم بدون ناقل في مربع الحوار.</span><span class="sxs-lookup"><span data-stu-id="9dc2e-111">However, a feature has been added that lets you hide non-carrier modes of delivery in the dialog box.</span></span> <span data-ttu-id="9dc2e-112">لتشغيل هذه الميزة، في الصفحة **معلمات Commerc** ، في علامة التبويب **أوامر العميل** ، عيِّن الخيار **إظهار خيارات وضع الناقل لأوامر الشحن فقط** على **نعم** .</span><span class="sxs-lookup"><span data-stu-id="9dc2e-112">To turn on this feature, on the **Commerce parameters** page, on the **Customer orders** tab, set the **Show only carrier mode options for ship orders** option to **Yes** .</span></span> <span data-ttu-id="9dc2e-113">بعد تشغيل هذه الميزة وتشغيل مهام التوزيع المناسبة لمزامنة المعلومات في قاعده بيانات القناة، لن تظهر أوضاع التسليم بدون ناقل للتحديد اثناء عملية إنشاء أوامر الشحن في نقطه البيع (POS).</span><span class="sxs-lookup"><span data-stu-id="9dc2e-113">After you turn on this feature and run the appropriate distribution jobs to sync the information to the channel database, non-carrier modes of delivery won't appear for selection during the process of creating shipment orders in POS.</span></span>
