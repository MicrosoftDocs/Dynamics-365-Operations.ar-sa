---
title: التحقق من صحة الشهادة NF-e مخصصة
description: يوفر هذا الموضوع معلومات حول تمكين شهادة NF-e مخصصة واستخدامها.
author: gionoder
ms.date: 10/06/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.custom: 97423
ms.assetid: ''
ms.search.region: Global
ms.author: janeaug
ms.search.validFrom: 2020-07-08
ms.dyn365.ops.version: AX 10.0.12
ms.openlocfilehash: 895513f51798a797ebf59f8a5be4f5cde006726d
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 04/01/2021
ms.locfileid: "5813958"
---
# <a name="nf-e-custom-certificate-validation"></a><span data-ttu-id="100e6-103">التحقق من صحة الشهادة NF-e مخصصة</span><span class="sxs-lookup"><span data-stu-id="100e6-103">NF-e custom certificate validation</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="100e6-104">عند تشغيل ميزه التحقق من صحة شهادة NF-e مخصصة، يسمح التحقق المخصص من الصحة بالاتصال بخدمات الويب.</span><span class="sxs-lookup"><span data-stu-id="100e6-104">When you turn the NF-e custom certificate verification feature, custom validation allows a connection with the web services.</span></span> <span data-ttu-id="100e6-105">هذا الاتصال مطلوب لإرسال NF-e واستلام التخويل من SEFAZ.</span><span class="sxs-lookup"><span data-stu-id="100e6-105">This connection is required to transmit NF-e and receive authorization from SEFAZ.</span></span>

<span data-ttu-id="100e6-106">يتم إصدار خاصيه **غرض مصادقه الخادم** من الشهادة V5 من قبل هيئه Brazilian Root Certificate Authority.</span><span class="sxs-lookup"><span data-stu-id="100e6-106">The **Server authentication purpose** property from the certificate V5 is issued by the Brazilian Root Certificate Authority.</span></span> <span data-ttu-id="100e6-107">يتم إيقاف تشغيل هذه الخاصية افتراضيا ويجب تمكينها يدويا.</span><span class="sxs-lookup"><span data-stu-id="100e6-107">This property is turned off by default and must be manually enabled.</span></span> <span data-ttu-id="100e6-108">في بعض الحالات، يمكن لتحديث الشهادة التلقائي تبديل هذه الخاصية إلى لم يعد ممكنا.</span><span class="sxs-lookup"><span data-stu-id="100e6-108">In some circumstances, the automatic certificate update can switch this property to no longer be enabled.</span></span> <span data-ttu-id="100e6-109">إذا حدث ذلك، فان اتصال TLS متأثر ولا يعد موثوقا به.</span><span class="sxs-lookup"><span data-stu-id="100e6-109">If this happens, the TLS connection is affected and is no longer trusted.</span></span> <span data-ttu-id="100e6-110">وتتاثر القدرة علي إصدار NF-e في بيئات الإنتاج لولايات ميناس جريس (MG) وولايات بارانا (PR) أيضا.</span><span class="sxs-lookup"><span data-stu-id="100e6-110">The ability to issue NF-e on production environments for states of Minas Gerais (MG) and Paraná (PR) states is also impacted.</span></span>

<span data-ttu-id="100e6-111">يسمح هذا التحديث بحل بديل للتحقق من صحة الشهادة، مما يعني انه من الممكن تاسيس اتصال آمن.</span><span class="sxs-lookup"><span data-stu-id="100e6-111">This update allows for an alternative solution for certificate validation, which means that it’s possible to establish a secure communication.</span></span>




[!INCLUDE[footer-include](../../includes/footer-banner.md)]