---
title: التعاون مع عملاء سلسلة التوريد الداخلية
description: يوضح هذا الإجراء كيفية عرض كافة الأوامر المخططة التي ستتم تلبيتها بواسطة مورّد بين شركات شقيقة.
author: ShylaThompson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: DefaultDashboard, ReqCreatePlanWorkspace, ReqTransPlanCard, ReqOutboundIntercompanyDemand
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 2746534cc808dc61e54aa55c1030422bb37e8984
ms.sourcegitcommit: fcb27d6a46cd544feef34f6ec7607bdd46b0c12b
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 03/18/2020
ms.locfileid: "3148137"
---
# <a name="collaborate-with-internal-supply-chain-customers"></a><span data-ttu-id="a2b06-103">التعاون مع عملاء سلسلة التوريد الداخلية</span><span class="sxs-lookup"><span data-stu-id="a2b06-103">Collaborate with internal supply chain customers</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="a2b06-104">يوضح هذا الإجراء كيفية عرض كافة الأوامر المخططة التي ستتم تلبيتها بواسطة مورّد بين شركات شقيقة.</span><span class="sxs-lookup"><span data-stu-id="a2b06-104">This procedure shows how to view all the planned orders that will be fulfilled by an intercompany vendor.</span></span> <span data-ttu-id="a2b06-105">شركة بيانات العرض التوضيحي التي تم استخدامها لإنشاء هذا الإجراء هي DEMF.</span><span class="sxs-lookup"><span data-stu-id="a2b06-105">The demo data company used to create this procedure is DEMF.</span></span>

1. <span data-ttu-id="a2b06-106">انقر فوق "التخطيط الرئيسي‬".</span><span class="sxs-lookup"><span data-stu-id="a2b06-106">Click Master planning.</span></span>
2. <span data-ttu-id="a2b06-107">في حقل "الخطة"، أدخل قيمة أو حددها.</span><span class="sxs-lookup"><span data-stu-id="a2b06-107">In the Plan field, enter or select a value.</span></span>
    * <span data-ttu-id="a2b06-108">في حقل "الخطة"، حدد "الخطة 10".</span><span class="sxs-lookup"><span data-stu-id="a2b06-108">In the Plan field, select plan 10.</span></span>  
3. <span data-ttu-id="a2b06-109">انقر فوق "تشغيل".</span><span class="sxs-lookup"><span data-stu-id="a2b06-109">Click Run.</span></span>
4. <span data-ttu-id="a2b06-110">في الحقل "عدد السلاسل"، أدخل رقمًا.</span><span class="sxs-lookup"><span data-stu-id="a2b06-110">In the Number of threads field, enter a number.</span></span>
    * <span data-ttu-id="a2b06-111">يمثل هذا عدد السلاسل المتوازية التي يجب استخدامها للتخطيط الرئيسي.</span><span class="sxs-lookup"><span data-stu-id="a2b06-111">This represents the number of parallel threads to be used for master planning.</span></span>  
5. <span data-ttu-id="a2b06-112">انقر فوق "موافق".</span><span class="sxs-lookup"><span data-stu-id="a2b06-112">Click OK.</span></span>
    * <span data-ttu-id="a2b06-113">قد يستغرق هذا الأمر بعض الوقت.</span><span class="sxs-lookup"><span data-stu-id="a2b06-113">This may take a while.</span></span>  
6. <span data-ttu-id="a2b06-114">انقر فوق "مطلب مخطط بين الشركات الشقيقة‬".</span><span class="sxs-lookup"><span data-stu-id="a2b06-114">Click Planned intercompany demand.</span></span>
7. <span data-ttu-id="a2b06-115">انقر فوق "مطلب صادر مخطط بين الشركات الشقيقة‬".</span><span class="sxs-lookup"><span data-stu-id="a2b06-115">Click Outbound planned intercompany demand.</span></span>
    * <span data-ttu-id="a2b06-116">توفر هذه الصفحة نظرة عامة حول المطلب المخطط بكامله الذي ستتم تلبيته بواسطة مورّد سلسلة التوريد الداخلية.</span><span class="sxs-lookup"><span data-stu-id="a2b06-116">This page provides an overview of all the planned demand that will be fulfilled by an internal supply chain vendor.</span></span>  
8. <span data-ttu-id="a2b06-117">قم بتوسيع مقطع "تفاصيل المطلب في المراحل التمهيدية‬"؟</span><span class="sxs-lookup"><span data-stu-id="a2b06-117">Expand the Upstream demand details section.</span></span>
    * <span data-ttu-id="a2b06-118">في هذا المقطع، يمكنك مشاهدة تفاصيل حول كيفية تلبية المطلب.</span><span class="sxs-lookup"><span data-stu-id="a2b06-118">In this section, you can see the details about how the demand will be fulfilled.</span></span> <span data-ttu-id="a2b06-119">قد تضطر إلى الانتظار ريثما يتم تشغيل التخطيط الرئيسي في شركة التوريد قبل أن تتمكن من رؤية معلومات إضافية هنا.</span><span class="sxs-lookup"><span data-stu-id="a2b06-119">You may need to wait for master planning to be run in the supply company before you can see additional information here.</span></span>  

