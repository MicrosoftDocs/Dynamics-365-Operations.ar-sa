---
title: التعاون مع عملاء سلسلة التوريد الداخلية
description: يوضح هذا الإجراء كيفية عرض كافة الأوامر المخططة التي ستتم تلبيتها بواسطة مورّد بين شركات شقيقة.
author: ShylaThompson
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: DefaultDashboard, ReqCreatePlanWorkspace, ReqTransPlanCard, ReqOutboundIntercompanyDemand
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 84c42e550d51e40b7f777c3da67ed765519ddfd0
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 10/13/2020
ms.locfileid: "4421390"
---
# <a name="collaborate-with-internal-supply-chain-customers"></a><span data-ttu-id="15e00-103">التعاون مع عملاء سلسلة التوريد الداخلية</span><span class="sxs-lookup"><span data-stu-id="15e00-103">Collaborate with internal supply chain customers</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="15e00-104">يوضح هذا الإجراء كيفية عرض كافة الأوامر المخططة التي ستتم تلبيتها بواسطة مورّد بين شركات شقيقة.</span><span class="sxs-lookup"><span data-stu-id="15e00-104">This procedure shows how to view all the planned orders that will be fulfilled by an intercompany vendor.</span></span> <span data-ttu-id="15e00-105">شركة بيانات العرض التوضيحي التي تم استخدامها لإنشاء هذا الإجراء هي DEMF.</span><span class="sxs-lookup"><span data-stu-id="15e00-105">The demo data company used to create this procedure is DEMF.</span></span>

1. <span data-ttu-id="15e00-106">انقر فوق "التخطيط الرئيسي‬".</span><span class="sxs-lookup"><span data-stu-id="15e00-106">Click Master planning.</span></span>
2. <span data-ttu-id="15e00-107">في حقل "الخطة"، أدخل قيمة أو حددها.</span><span class="sxs-lookup"><span data-stu-id="15e00-107">In the Plan field, enter or select a value.</span></span>
    * <span data-ttu-id="15e00-108">في حقل "الخطة"، حدد "الخطة 10".</span><span class="sxs-lookup"><span data-stu-id="15e00-108">In the Plan field, select plan 10.</span></span>  
3. <span data-ttu-id="15e00-109">انقر فوق "تشغيل".</span><span class="sxs-lookup"><span data-stu-id="15e00-109">Click Run.</span></span>
4. <span data-ttu-id="15e00-110">في الحقل "عدد السلاسل"، أدخل رقمًا.</span><span class="sxs-lookup"><span data-stu-id="15e00-110">In the Number of threads field, enter a number.</span></span>
    * <span data-ttu-id="15e00-111">يمثل هذا عدد السلاسل المتوازية التي يجب استخدامها للتخطيط الرئيسي.</span><span class="sxs-lookup"><span data-stu-id="15e00-111">This represents the number of parallel threads to be used for master planning.</span></span>  
5. <span data-ttu-id="15e00-112">انقر فوق "موافق".</span><span class="sxs-lookup"><span data-stu-id="15e00-112">Click OK.</span></span>
    * <span data-ttu-id="15e00-113">قد يستغرق هذا الأمر بعض الوقت.</span><span class="sxs-lookup"><span data-stu-id="15e00-113">This may take a while.</span></span>  
6. <span data-ttu-id="15e00-114">انقر فوق "مطلب مخطط بين الشركات الشقيقة‬".</span><span class="sxs-lookup"><span data-stu-id="15e00-114">Click Planned intercompany demand.</span></span>
7. <span data-ttu-id="15e00-115">انقر فوق "مطلب صادر مخطط بين الشركات الشقيقة‬".</span><span class="sxs-lookup"><span data-stu-id="15e00-115">Click Outbound planned intercompany demand.</span></span>
    * <span data-ttu-id="15e00-116">توفر هذه الصفحة نظرة عامة حول المطلب المخطط بكامله الذي ستتم تلبيته بواسطة مورّد سلسلة التوريد الداخلية.</span><span class="sxs-lookup"><span data-stu-id="15e00-116">This page provides an overview of all the planned demand that will be fulfilled by an internal supply chain vendor.</span></span>  
8. <span data-ttu-id="15e00-117">قم بتوسيع مقطع "تفاصيل المطلب في المراحل التمهيدية‬"؟</span><span class="sxs-lookup"><span data-stu-id="15e00-117">Expand the Upstream demand details section.</span></span>
    * <span data-ttu-id="15e00-118">في هذا المقطع، يمكنك مشاهدة تفاصيل حول كيفية تلبية المطلب.</span><span class="sxs-lookup"><span data-stu-id="15e00-118">In this section, you can see the details about how the demand will be fulfilled.</span></span> <span data-ttu-id="15e00-119">قد تضطر إلى الانتظار ريثما يتم تشغيل التخطيط الرئيسي في شركة التوريد قبل أن تتمكن من رؤية معلومات إضافية هنا.</span><span class="sxs-lookup"><span data-stu-id="15e00-119">You may need to wait for master planning to be run in the supply company before you can see additional information here.</span></span>  

